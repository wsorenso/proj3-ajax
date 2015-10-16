Here are the ACP rules:
	The opening times for checkpoints are calculated using the max speeds for each distance interval, as well as the distance from the start of the race that the current checkpoint is.
	The opening time for a checkpoint would be the sum of the quickest times that each distance interval could be covered up to the interval containing our current checkpoint, plus the remaining distance traveled at the max speed for the last distance interval.
	Here is the algorithm:

	openingTime(distance) // gives us the opening time for a station at a given distance

	if(distance <= 200)
		opening_time = distance / 34;

	else if(distance > 200 && distance <= 400)
		opening_time = 200/34 + ((distance - 200)/32);

	else if(distance > 400 && distance <= 600)
		opening_time = 200/34 + 200/32 + ((distance - 400)/30);

	else if(distance > 600 && distance <= 1000)
		opening_time = 200/34 + 200/32 + 200/30 + ((distance - 600)/28);

	return opening_time;


The closing time for the first checkpoint (the start line) is always one hour after the race starts.
Closing times are calculated in much the same way as start times, except that the minimum speeds are used.


ISSUES:
	I was never able to get my page runnable on ix and spent the entire project working on that. This means that I have almost no changes made to the original template, and there is no testable functionality. A very frustrating way to spend the last few study sessions!

