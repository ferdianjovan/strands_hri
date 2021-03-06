^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package strands_human_aware_navigation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

0.0.5 (2014-11-11)
------------------

0.0.3 (2014-11-06)
------------------

0.0.2 (2014-10-31)
------------------

0.0.1 (2014-10-31)
------------------
* Removed calls to strands_head_orientation as those won't work in a release version.
* Added missing webpage
* Prepared strands_human_aware_navigation for release.
* Renamed strands_people_tracker to bayes_people_tracker
* strands_perception_people_msgs has been removed
* Adapting to new people_tracker message.
* Merge branch 'hydro-devel' into people_tracker
  Conflicts:
  strands_human_aware_navigation/src/scripts/human_aware_navigation.py
* Adapting the human_aware_velocity to the new topic name and type of the people tracker
* running head orientation while human_aware_navigation is running. Only if present. Changed default timeout of engaged server.
* Changing default parameters back to be more social.
* Changed default params
* Setting initial gaze goal for the nav_goal
  resetting the mode in the behaviour switch to prevent it from looking away.
* If human detected, look at human
  else look at nav goal
* Not changing rotational velocity.
* Hard coding "fast" values.
* changes to human aware navigation to handle new goals wothout outputting failure
* Cancelling the gaze goal if move_base is successful.
* Catching service exception for reconfigure.
  Using gaze_at_pose to lock at nav goal.
* Bug fix: subscribing before creating the action server leaad to errors due to checking for a non existing action server in the callback.
* Merge pull request #39 from cdondrup/hydro-devel
  Bug fix. Using dictionary of read parameters now. Needed changing in the...
* Bug fix. Using dictionary of read parameters now. Needed changing in the callback.:w
* Creating action server after every client has been created
* Minor bug fix: Preempting triggered an error because it still tried to set the goal as aborted.
  Also moved a lot of output to debug level or removed it completely.
* Piping through move_base result and feedback.
  Currently move_base does not publish a result though.
* Adapted human_aware_navigation to be used as navigation action server in topological map.
* Contributors: Bruno Lacerda, Christian Dondrup, cdondrup, strands
