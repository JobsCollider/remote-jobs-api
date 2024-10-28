
# Remote Jobs API

## About JobsCollider

JobsCollider hosts one of the largest collections of remote and work-from-home job listings.
Check out our website at [JobsCollider](https://jobscollider.com/) to browse through tens of thousands opportunities across various categories and industries.

We also provide [Remote Jobs RSS](https://github.com/jobscollider/remote-jobs-rss).

## Access and Usage Rules

- **Do not submit jobs from JobsCollider to third-party websites**, such as LinkedIn Jobs or Google Jobs.
- **Link back to the JobsCollider URL and mention JobsCollider as a source** when using our feeds.
- **Failure to follow these rules may result in denial of access** to the feeds.

## API Endpoints

### Search Remote Jobs

Search for remote jobs by providing a search query and/or a category.

`Please note that the search results are delayed by 24 hours, updated hourly, and limited to 2000 jobs. Interested in unlimited and private API access? We offer a paid plan.`

- **Method**: `GET`
- **Endpoint**: `https://jobscollider.com/api/search-jobs`
- **Query Parameters**:
  - `query` (optional): Search query to match against job title
  - `category` (optional): Job category, one of: 
    - `software_development`
    - `cybersecurity`
    - `customer_service` 
    - `design`
    - `marketing` 
    - `sales`
    - `product` 
    - `business` 
    - `data`
    - `devops` 
    - `finance_legal` 
    - `human_resources` 
    - `qa`
    - `writing` 
    - `project_management` 
    - `all_others`
- **Response**: JSON object with the following fields:
  - `_README_` (string): API usage instructions
  - `jobs_count` (int): Number of jobs found
  - `jobs` (array): List of job objects
    - `id` (string): Job ID
    - `url` (string): Job URL
    - `company_name` (string): Company name
    - `company_logo` (string, optional): Company logo URL
    - `title` (string): Job title
    - `category` (string): Job category
    - `seniority` (string): Job seniority
    - `description` (string): Job description
    - `salary_min` (int, optional): Minimum salary in USD per year, if available
    - `salary_max` (int, optional): Maximum salary in USD per year, if available
    - `locations` (array): List of job locations
    - `published_at` (string): Job publication date in RFC3339 format

## Contact Us

If you have any questions or need further assistance, feel free to reach out to us at [hello@jobscollider.com](mailto:hello@jobscollider.com)
