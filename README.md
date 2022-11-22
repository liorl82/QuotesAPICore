# Execute the following from the current directory to start the QuotesApi service
docker build -t quotesapi .
docker run -it --rm -p 5000:80 --name quotesapiapp docker build -t quotesapi .

# Then execute your request, e.g.:
curl -X 'GET' \
  'http://localhost:32108/api/Quote?from_currency_code=EUR&amount=100&to_currency_code=ILS' \
  -H 'accept: text/plain'
