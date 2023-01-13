# AI-HealthRecover

The challenge was to update the game and add couple new functionalities such as an action to hide/flee when the health bar is too low (thershold defined in the tree), wait until is recharge to certain value and return to the last position where player was seen. These are the steps followed:

1. Update the .BT file to add a new tree for the return action. Then, add the health conditions and update the sequence with the new action (void in the AI.cs file)
2. Also, call the new tree from the prio tree "patrol".
3. Then next action to implement was hide/flee from the player. For that one, several trees needs to be updated such as "Attack", "Look Around" and "Wander". It's intorduces in these trees accoring to the condition/rules we might need in each case. 
3. Finally, last update to the .BT file is the Flee status. Two trees needs to be updated: "LookAround" and the new tree we just added on step 1"ReturnToLastPositionOfPlayer". Also, condition (true/false) needs to be used according to the sequence. 


Now that we have our .BT file complete, we need to include the new tasks in the AI.cs file. These are the steps followed:

1. Create two new variables: the fleeStatus and the Vector3 which will detect the last position of the player.
2. Add the 3 new methods/tasks:
  a. we use a void to create the action for the enemy to return to the last position of the player. We use the vestor3 we've just created.
  b. we use a bool for the flee status by simply relating the variables flee status with the status
  c. we use another bool to create the fleeing action. 
 3. Ensure that naming are all correct and the same between the two files.
 4. Test it!
 5. Play and enjoy 
  
