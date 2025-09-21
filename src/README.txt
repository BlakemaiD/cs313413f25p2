TestList.java and TestIterator.java

	TODO also try with a LinkedList - does it make any difference?

		It works with the LinkedList method as well as the ArrayList.
		From what I saw, there was no difference, the tests passed using both.

TestList.java

	testRemoveObject()

		list.remove(5); // what does this method do?

			This method above removes the element at index 5

		list.remove(Integer.valueOf(5)); // what does this one do?

			This method removes the first integer with the value of 5

TestIterator.java

	testRemove()

		i.remove(); // what happens if you use list.remove(77)?

		The i.remove() method takes out the last integer/element returned by the .next() method.
		If you use list.remove(77), you will remove the first element that has the integer 77.

TestPerformance.java

	State how many times the tests were executed for each SIZE (10, 100, 1000 and 10000)
	to get the running time in milliseconds and how the test running times were recorded.

	The tests were done multiple time for each size. The running time was measured using System.nanoTime();
	Source used for help: https://www.tutorialspoint.com/java/lang/system_nanotime.htm
	I copied the results into the table below.

	SIZE 10
								  #1   #2   #3   #4   #5   #6
        testArrayListAddRemove:   12   13   12 (fill these in in ms)
        testLinkedListAddRemove:  11   12   12
		testArrayListAccess:      5    4    5
        testLinkedListAccess:     4    5    5

	SIZE 100
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:   20   20   21     ... (fill these in in ms)
        testLinkedListAddRemove:  11   11   12
		testArrayListAccess:      5    4    5
        testLinkedListAccess:     12   11   12

	SIZE 1000
								  #1   #2    #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  100   112   115   ... (fill these in in ms)
        testLinkedListAddRemove: 13    13    14
		testArrayListAccess:     5      3    4
        testLinkedListAccess:    281   288  290

	SIZE 10000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  938   963  950     ... (fill these in in ms)
        testLinkedListAddRemove: 11    12    12
		testArrayListAccess:     4     4     5
        testLinkedListAccess:    4026  4031  4050

	listAccess - which type of List is better to use, and why?

		ArrayList is much better with access times, through all the tests, the time has been consistently low.
		This is because the access time for ArrayList is O(1).
		LinkedList time increased significantly when the size increased. This is becasue LinkedList is
		O(n) so it will need to access each node.

	listAddRemove - which type of List is better to use, and why?

		LinkedList is better to use for add/remove becasue the change of nodes and heads are O(1).
		The time for LinkedList has been consistant with all the tests.
		ArrayList has to shift all the values when there is a removal or an addition, this makes it O(n).