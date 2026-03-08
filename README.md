Before running `midterm.qmd`, please follow these setup steps first:

### 1. Install Dependencies

Install the required Python packages from `requirements.txt`:

```bash
pip install -r requirements.txt
```

### 2. Configure RAWG API Key

1. Visit the [RAWG Video Games Database API](https://rawg.io/apidocs) website
2. Register for an account and obtain your API key
3. Create a `.env` file in the project root directory
4. Add the following line to the `.env` file:

```
API_KEY=your_rawg_api_key_here
```

## Notes

The project uses cached data files to avoid repeated API calls. If cache files exist, the notebook will load data from disk instead of making new API requests, but you can choose to delete the csv files to test the API call. 

Also there are a heavy limit on these two APIs: 
- The SteamSpy API allows one request per page per minute.
- The RAWG API has a rate limit of 20,000 requests per three months.