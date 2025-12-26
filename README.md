# employees-details
def get_employee_details():
    name = input("Enter Employee Name: ")
    emp_id = input("Enter Employee ID: ")
    department = input("Enter Department: ")
    basic_salary = float(input("Enter Basic Salary: "))
    return name, emp_id, department, basic_salary


def calculate_salary(basic_salary):
    hra = basic_salary * 0.20     # 20% House Rent Allowance
    da = basic_salary * 0.10      # 10% Dearness Allowance
    pf = basic_salary * 0.12      # 12% Provident Fund deduction

    gross_salary = basic_salary + hra + da
    net_salary = gross_salary - pf

    return hra, da, pf, gross_salary, net_salary


def print_salary_slip(name, emp_id, department, basic, hra, da, pf, gross, net):
    print("\n============== EMPLOYEE SALARY SLIP ==============")
    print("Employee Name   :", name)
    print("Employee ID     :", emp_id)
    print("Department      :", department)
    print("-----------------------------------------------")
    print("Basic Salary    : Rs.", basic)
    print("HRA (20%)       : Rs.", hra)
    print("DA (10%)        : Rs.", da)
    print("PF Deduction    : Rs.", pf)
    print("-----------------------------------------------")
    print("Gross Salary    : Rs.", gross)
    print("Net Salary      : Rs.", net)
    print("================================================")


name, emp_id, department, basic = get_employee_details()
hra, da, pf, gross, net = calculate_salary(basic)
print_salary_slip(name, emp_id, department, basic, hra, da, pf, gross, net)

output
Enter Employee Name: Anjali
Enter Employee ID: E102
Enter Department: HR
Enter Basic Salary: 25000



============== EMPLOYEE SALARY SLIP ==============
Employee Name   : Anjali
Employee ID     : E102
Department      : HR
-----------------------------------------------
Basic Salary    : Rs. 25000.0
HRA (20%)       : Rs. 5000.0
DA (10%)        : Rs. 2500.0
PF Deduction    : Rs. 3000.0
-----------------------------------------------
Gross Salary    : Rs. 32500.0
Net Salary      : Rs. 29500.0
================================================
