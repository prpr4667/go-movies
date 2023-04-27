**GET ALL MOVIES**:

curl --location --request GET 'http://localhost:8000/movies'
<br/>
<br/>

**GET MOVIE BY NAME**:<br/>
curl --location --request GET 'http://localhost:8000/movies/Movie 1'
<br/>
<br/>

**CREATE MOVIE**:<br/>
curl --location --request POST 'http://localhost:8000/movies' \
--header 'Content-Type: application/json' \
--data-raw `json'{
    "Isbn": "55",
    "Title": "Movie 5",
    "Director": {
        "Firstname": "First5",
        "Lastname": "Last5"
    }
}'`
<br/>
<br/>

**UPDATE MOVIE BY NAME**:<br/>
curl --location --request PUT 'http://localhost:8000/movies/Movie 5' \
--header 'Content-Type: application/json' \
--data-raw `json'{
    "Isbn": "55_1",
    "Title": "Movie 5",
    "Director": {
        "Firstname": "First5",
        "Lastname": "Last5"
    }
}'`
<br/>
<br/>

**DELETE MOVIE BY NAME**:<br/>
curl --location --request DELETE 'http://localhost:8000/movies/Movie 5'
