## Setup 🖥️

1. Install Ruby latest version 💎
- If you use **Mac🍎 or any Linux Distro🐧**, we suggest you use a ruby package manager like rbenv or rvm. You can follow instruction here - https://www.ruby-lang.org/en/documentation/installation/
- If you are using **Windows 10**, we suggest you setup your machine using Docker Desktop + WSL2 + VSCode, More info here - https://code.visualstudio.com/docs/remote/containers
2. Install Bundler - https://bundler.io/
3. CREATE A NEW REPO in github
4. Add this README file on your new repo
5. Create a new branch, use this format `feature/BRANCH_NAME`
6. Add a unit test framework 🧪
- **Rspec** - https://semaphoreci.com/community/tutorials/getting-started-with-rspec
- **Minitest** - https://semaphoreci.com/community/tutorials/getting-started-with-minitest

If you have any question or clarification please create an issue on the main repository.

## What do we expect? ✔️

That you are able to:
- ✔️learn enough ruby to complete the requirements.
- ✔️create a repo, branch, separate pull requests and change the base of each branch using git and github. 
- ✔️multiple small commits with good commit message. We are more interested on your thought processes rather than the final code.
- ✔️write unit tests and cover all the examples computation on the requirements.
- ✔️design and create solution using OOP especially the algorithm of the requirement#1.
- ✔️use atleast 1 design pattern - https://www.oodesign.com/
- ✔️create a working REST API - https://en.wikipedia.org/wiki/Representational_state_transfer
- ✔️use postman to discuss your API - https://www.postman.com/
- ✔️do a CRUD to a database

## Requirements 📝
please create 1 feature branch per requirement and create 1 pull request per feature branch and update the base branch of the previous requirement/feature branch. So in the end you have 4 pull request in total per requirement - https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/changing-the-base-branch-of-a-pull-request

| base branch | feature branch |
|----------|:-------------:|
| master| requirement 1 |
| requirement 1| requirement 2 |
| requirement 2| requirement 3 |
| requirement 3| requirement 4 |

**1. You are tasked to create a ruby function `generate_monthly_payslip` to compute a monthly payslip of an individual based on his annual salary with 2 decimal places with unit tests.**

Example:

When you give an argument of "Ren" and "60000"

`generate_monthly_payslip "Ren" 60000`

Then it will return an output in console:

```
 Monthly Payslip for: "Ren"
 Gross Monthly Income: $5000.00
 Monthly Income Tax: $500.00
 Net Monthly Income: $4500.00
```

### The Tax Bracket is as follows

| Salary Bracket | Rate |
|----------|:-------------:|
| first 0 - 20000 | 0% |
| next 20001-40000 | 10% |
| next 40001-80000 | 20% |
| next 80001-180000 | 30% |
| 180001 and above | 40% |

### Sample Tax Computation 1

Annual Salary 60000

| Salary Bracket | Rate | Taxable Amount | Total Tax |
|---|---|---|---|
| first 0 - 20000 | 0% | 20000 | 0 |
| next 20001-40000 | 10% | 20000 | 2000 |
| next 40001-80000 | 20% | 20000 | 4000 |
| next 80001-180000 | 30% | 0 | 0 |
| 180001 and above | 40% | 0 | 0 |
| **Total** | | 60000 | 6000 |

### Sample Tax Computation 2

Annual Salary 200000

| Salary Bracket | Rate | Taxable Amount | Total Tax |
|---|---|---|---|
| first 0 - 20000 | 0% | 20000 | 0 |
| next 20001-40000 | 10% | 20000 | 2000 |
| next 40001-80000 | 20% | 40000 | 8000 |
| next 80001-180000 | 30% | 100000 | 30000 |
| 180001 and above | 40% | 20000 | 8000 |
| **Total** | | 200000 | 48000 |

### Sample Tax Computation 3

Annual Salary 80150

| Salary Bracket | Rate | Taxable Amount | Total Tax |
|---|---|---|---|
| first 0 - 20000 | 0% | 20000 | 0 |
| next 20001-40000 | 10% | 20000 | 2000 |
| next 40001-80000 | 20% | 40000 | 8000 |
| next 80001-180000 | 30% | 150 | 45 |
| 180001 and above | 40% | 0 | 0 |
| **Total** | | 80150 | 10045 |

**2. Create a `POST` REST API request to expose your function. Request parameters should include employee_name and annual_salary. The response body should return JSON format. Add unit tests where you think its relevant.**
You can use:
- Rails - https://rubyonrails.org/
- Sinatra - http://sinatrarb.com/
```
{
  "employee_name": string,
  "gross_monthly_income": string,
  "monthly_income_tax": string,
  "net_monthly_income": string,
}
```

**3. When compute monthly salary POST API is invoked, Then write the following information in a database of your choice, you can use any local or cloud database**
- Timestamp
- Employee Name
- Annual Salary
- Monthly Income Tax

**4. Create a GET API to list out all information from Requirement 4 on JSON Format:**
- unit tests where you think its relevant
```
{
  salary_computations: [
    {
      "time_stamp": string,
      "employee_name": string
      "annual_salary": string
      "monthly_income_tax": string
    }
  ]
}
```

## Instructions ✔️
When you are done, tag me on your pull request 24 hours before the date our people team specified for the code review

Please come prepared to the code review about your approach:
- [ ] algorithm for payslip computation
- [ ] design pattern you used
- [ ] unit tests you wrote
- [ ] post/ get api / postman
- [ ] database you used

## Fave Engineering Culture 🧍🧍🧍

We just did a video and shared about our product and engineering culture you can [find it here](https://www.linkedin.com/posts/fave-group_wearefave-digitalproduct-product-activity-6592343555904245760-tlQm)

