
# Pagination

This project contains tasks for learning to paginate data.

## Tasks To Complete

| Task No. | Task Name                              | Description                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0        | **Simple helper function**             | [0-simple_helper_function.py](0-simple_helper_function.py) contains a Python function named `index_range` that takes two integer arguments `page` and `page_size` and returns a tuple of size two containing a start index and an end index corresponding to the range of indexes to return in a list for those particular pagination parameters. Page numbers are 1-indexed, i.e., the first page is page 1. |
| 1        | **Simple pagination**                  | [1-simple_pagination.py](1-simple_pagination.py) contains a Python script that implements a method named `get_page` to paginate a dataset of popular baby names using the `index_range` function. It verifies arguments with `assert`, uses the CSV file [Popular_Baby_Names.csv](Popular_Baby_Names.csv), and returns the appropriate page of the dataset.                                                               |
| 2        | **Hypermedia pagination**              | [2-hypermedia_pagination.py](2-hypermedia_pagination.py) contains a Python script that implements a `get_hyper` method, which returns a dictionary with various key-value pairs such as `page_size`, `page`, `data`, `next_page`, `prev_page`, and `total_pages`. It reuses the `get_page` method from the previous task.                                                        |
Sure, here are the project details for your README.md:

---

## Project Details

1. **Simple helper function**: 
   - Implement a function named `index_range` that takes two integer arguments `page` and `page_size`. 
   - The function returns a tuple of size two containing a start index and an end index corresponding to the range of indexes to return in a list for those particular pagination parameters.
   - Page numbers are 1-indexed, i.e., the first page is page 1.

2. **Simple pagination**:
   - Create a class `Server` to paginate a dataset of popular baby names.
   - Implement a method named `get_page` that takes two integer arguments `page` with default value 1 and `page_size` with default value 10.
   - Use `index_range` to find the correct indexes to paginate the dataset correctly and return the appropriate page of the dataset.
   - Ensure that if the input arguments are out of range for the dataset, an empty list is returned.
   - Use `assert` to verify that both arguments are integers greater than 0.

3. **Hypermedia pagination**:
   - Extend the `Server` class to include a method named `get_hyper`.
   - The `get_hyper` method takes the same arguments as `get_page` and returns a dictionary with the following key-value pairs:
     - `page_size`: the length of the returned dataset page.
     - `page`: the current page number.
     - `data`: the dataset page (equivalent to the return value from `get_page`).
     - `next_page`: number of the next page, `None` if no next page.
     - `prev_page`: number of the previous page, `None` if no previous page.
     - `total_pages`: the total number of pages in the dataset as an integer.
   - Ensure that `get_page` is reused in the implementation.

4. **Deletion-resilient hypermedia pagination**:
   - Modify the `Server` class to handle deletion-resilient pagination.
   - Implement a `get_hyper_index` method with two integer arguments: `index` with a `None` default value and `page_size` with default value of 10.
   - The method returns a dictionary with the following key-value pairs:
     - `index`: the current start index of the return page.
     - `next_index`: the next index to query with.
     - `page_size`: the current page size.
     - `data`: the actual page of the dataset.
   - Ensure that `index` is in a valid range using `assert`.
   - Handle cases where rows have been deleted from the dataset between queries, ensuring the user does not miss items when changing pages.

---| 3        | **Deletion-resilient hypermedia pagination** | [3-hypermedia_del_pagination.py](3-hypermedia_del_pagination.py) contains a Python script that implements a `get_hyper_index` method to provide deletion-resilient pagination. It returns a dictionary with key-value pairs such as `index`, `next_index`, `page_size`, and `data`, ensuring the user does not miss items from the dataset when changing pages.                               |
