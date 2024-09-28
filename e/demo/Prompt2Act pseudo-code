Require: Initial visual observation v_1, a user prompt L, and skill set Π.
$v_t$ represents the visual observation at time step $t$, $\mathcal{P}_{user}$ represents the user's prompt command, and $\Psi$ represents the predefined action functions. Each step $s_t$ is a small range text command that specifies a sub-task, which can be mapped to a predefined action function $\psi_{s_t} \in \Psi$, or to a code generation policy $\pi_{s_t} \in \Pi$.

1: t = 1, current_step = ∅
2: while current_step ≠ "done" do
3:     # Step 1: Visual segmentation and object recognition using SAM and GPT-4V
4:     segmented_regions = SAM_Model.segment(x_t)  # Use SAM to segment the image
5:     identified_objects = GPT4V_Model.identify(segmented_regions)  # Use GPT-4V to identify objects in the regions
       
6:     # Step 2: Chain-of-Thought (CoT) reasoning to generate the task plan
7:     if t == 1 then  # Generate the task plan only once based on user instruction L
8:         task_plan = VG_Marker.Plan(L, identified_objects)  # Visual grounding-based task plan
9:     end if

10:    # Step 3: Get the next action from the task plan
11:    next_action = task_plan[t]  # Retrieve the next action from task plan, e.g., pick, place
12:    Execute(next_action, x_t)  # Execute the robot action (e.g., pick up object, place object)

13:    # Step 4: Visual feedback to check completion of the action
14:    x_t+1 = Visual_Feedback()  # Get updated visual feedback after execution
15:    t = t + 1
16:    if TaskComplete(x_t+1) then  # Check if all steps of the task plan are completed
17:        current_step = "done"  # Task is complete
18:    else
19:        current_step = task_plan[t]  # Move to the next step in the task plan
20:    end if
21: end while
