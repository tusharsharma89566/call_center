# Call Center

A simple call center management system designed to organize and streamline call handling for customer service teams. This project demonstrates basic object-oriented principles, queue management, and a modular approach that can be extended for real-world applications.

## Features

- **Employee Hierarchy:** Supports multiple levels of employees (e.g., Respondent, Manager, Director).
- **Call Assignment:** Automatically routes calls to the lowest available employee level.
- **Call Queuing:** Queues calls if no employees are available and assigns them as employees become free.
- **Extensibility:** Modular design makes it easy to add new features or extend employee roles.

## Getting Started

### Prerequisites

- Python 3.x

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/tusharsharma89566/call_center.git
    cd call_center
    ```

2. (Optional) Set up a virtual environment:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

### Usage

1. Run the main script (replace `main.py` with the entry point if different):
    ```bash
    python main.py
    ```

2. Follow the command-line prompts to simulate incoming calls and employee assignments.

## Project Structure

```plaintext
call_center/
├── employee.py      # Employee class definitions and hierarchy
├── call.py          # Call class and call queue management
├── call_center.py   # CallCenter logic for routing calls
├── main.py          # Example usage and system simulation
├── README.md
```

## Example

```python
from call_center import CallCenter, Employee, Call

# Create employees
employees = [
    Employee("Alice", "Respondent"),
    Employee("Bob", "Manager"),
    Employee("Charlie", "Director"),
]

# Initialize call center
center = CallCenter(employees)

# Add incoming calls
center.receive_call(Call("Customer 1"))
center.receive_call(Call("Customer 2"))
```

## Contributing

Contributions are welcome! Please open issues or submit pull requests for enhancements or bug fixes.

## License

This project is licensed under the MIT License.

## Author

[Tushar Sharma](https://github.com/tusharsharma89566)
