# opener-docker-pos-tagger

Dockerfile for OpeNER part-of-speech tagger service.

Run and test locally:

```bash
docker run -p 8080:80 cwolff/opener-docker-language-identifier
docker run -p 8081:80 cwolff/opener-docker-tokenizer
docker run -p 8082:80 cwolff/opener-docker-pos-tagger

text="I went to Rome last year. It was fantastic."
text="$(curl -d "input=$text" http://localhost:8080)"
text="$(curl -d "input=$text" http://localhost:8081)"
curl -d "input=$text" http://localhost:8082
```
