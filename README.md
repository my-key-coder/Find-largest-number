# Find-largest-number
def largest_num(numbers):
  """
  This function finds the k-th largest number in a given list.

  Args:
    numbers: A list of numbers.

  Returns:
    The k-th largest number in the list.
  """
  list1 = list(numbers)  # Create a copy of the input list
  list2 = list(sorted(list1))  # Create a sorted copy of the list

  print(list2)  # Print the sorted list for reference

  k = int(input("Which largest number you want to find: "))  # Get the desired rank from the user

  a = len(list2)  # Get the length of the sorted list

  if k == 1:
    # If the user wants the largest number, directly print the last element
    print(list2[a-1]) 
  else:
    # Remove k-1 elements from the end of the sorted list
    for _ in range(k-1):
      list2.pop() 
    print(list2[a-k])  # Print the k-th largest element

# Example usage
num = [1, 22, 83, 110, 83, 2, 6, 9, 74, 65, 67]
largest_num(num)
