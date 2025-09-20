COMP 313/413 Project 2 Report Using the Template

TestList.java and TestIterator.java

	TODO also try with a LinkedList - does it make any difference?

      No it does not make any difference at all, at least from the initial test pass/fail.

TestList.java

	testRemoveObject()

		list.remove(5); // what does this method do?

		      //removes the element at index 5 which is the third 77


		list.remove(Integer.valueOf(5)); // what does this one do?

      //removes the first instance of the object int 5

TestIterator.java

	testRemove()

		i.remove(); // what happens if you use list.remove(77)?

		    What happens is the first matching element in the list is removed, but then get an exception because
            the list is being modified outside of the iterator while running.

TestPerformance.java

    State how many times the tests were executed for each SIZE (10, 100, 1000 and 10000)
    to get the running time in milliseconds and how the test running times were recorded.

    SIZE 10
    Tests 1-7
                                #1   #2   #3    #4    #5    #6    #7
    testArrayListAddRemove:  0.017 0.017 0.017 0.017 0.016 0.017 0.017
    testLinkedListAddRemove: 0.015 0.015 0.014 0.014 0.015 0.015 0.015
    testArrayListAccess:     0.009 0.010 0.010 0.010 0.010 0.010 0.009
    testLinkedListAccess:    0.005 0.006 0.006 0.006 0.005 0.007 0.006

    SIZE 100
                                #1   #2   #3    #4    #5    #6    #7
    testArrayListAddRemove:  0.026 0.032 0.025 0.026 0.025 0.025 0.025
    testLinkedListAddRemove: 0.017 0.016 0.014 0.014 0.015 0.025 0.017
    testArrayListAccess:     0.009 0.017 0.014 0.013 0.010 0.011 0.010
    testLinkedListAccess:    0.022 0.019 0.018 0.018 0.018 0.018 0.018

    SIZE 1000
                                #1   #2   #3    #4    #5    #6    #7
    testArrayListAddRemove:  0.151 0.151 0.152 0.166 0.151 0.151 0.152
    testLinkedListAddRemove: 0.015 0.015 0.014 0.014 0.015 0.014 0.014
    testArrayListAccess:     0.024 0.014 0.021 0.017 0.010 0.011 0.010
    testLinkedListAccess:    0.368 0.365 0.371 0.371 0.366 0.364 0.369

    SIZE 10000
                              #1    #2    #3    #4    #5    #6    #7
    testArrayListAddRemove:  1.593 1.589 1.611 1.616 1.561 1.623 1.646
    testLinkedListAddRemove: 0.016 0.015 0.017 0.016 0.016 0.016 0.018
    testArrayListAccess:     0.010 0.012 0.007 0.010 0.012 0.015 0.011
    testLinkedListAccess:    4.848 4.861 4.851 4.914 4.983 4.884 4.892

    Size 100000
                                #1      #2      #3      #4      #5      #6      #7
    testArrayListAddRemove:   17.795  17.582  17.625  17.764  17.648  17.739  17.638
    testLinkedListAddRemove:  0.021   0.020   0.018   0.023   0.022   0.021   0.024
    testArrayListAccess:      0.018   0.017   0.017   0.018   0.018   0.021   0.017
    testLinkedListAccess:     48.636  48.232  49.204  49.167  50.037  49.367  48.349
    listAccess - which type of List is better to use, and why?

    ArrayList is better for access because it provides O(1) time for random access using indices,
    while LinkedList requires O(n) time to traverse the list to reach an element.

    listAddRemove - which type of List is better to use, and why?

    LinkedList is better for frequent add/remove operations, especially in the middle of the list,
    because it can insert or remove elements in O(1) time (once the node is reached), whereas ArrayList may require shifting elements, which is O(n) time.

