## Informações sobre o exercício "Desafio de CI" (05/08/2020)

Arquivos:<br />
- cloudbuild.yaml<br />
- Dockerfile <br />
- soma.go<br />
- soma_test.go<br />
<br />
Endereço do build: https://console.cloud.google.com/cloud-build/builds/b56059fd-b634-44d3-9da6-6525c4aceeb6?project=codeeducation-test-285316&pli=1<br />
<br />

Log do build abaixo e também em evidencias/Build.log. <br />

<pre><code>
starting build "b56059fd-b634-44d3-9da6-6525c4aceeb6"

FETCHSOURCE
Fetching storage object: gs://80868692064.cloudbuild-source.googleusercontent.com/7af8cfba38de17b5e28a754aef6daab23b5285f7-1ddc28b7-2263-4cce-b1df-050971d7da46.tar.gz#1596674099736832
Copying gs://80868692064.cloudbuild-source.googleusercontent.com/7af8cfba38de17b5e28a754aef6daab23b5285f7-1ddc28b7-2263-4cce-b1df-050971d7da46.tar.gz#1596674099736832...
/ [0 files][    0.0 B/  1.0 KiB]                                                
/ [1 files][  1.0 KiB/  1.0 KiB]                                                
Operation completed over 1 objects/1.0 KiB.                                      
BUILD
Starting Step #0 - "Executando build e subindo imagem para GCR privado"
Step #0 - "Executando build e subindo imagem para GCR privado": Already have image (with digest): gcr.io/cloud-builders/docker
Step #0 - "Executando build e subindo imagem para GCR privado": 
Step #0 - "Executando build e subindo imagem para GCR privado":                    ***** NOTICE *****
Step #0 - "Executando build e subindo imagem para GCR privado": 
Step #0 - "Executando build e subindo imagem para GCR privado": Alternative official `docker` images, including multiple versions across
Step #0 - "Executando build e subindo imagem para GCR privado": multiple platforms, are maintained by the Docker Team. For details, please
Step #0 - "Executando build e subindo imagem para GCR privado": visit https://hub.docker.com/_/docker.
Step #0 - "Executando build e subindo imagem para GCR privado": 
Step #0 - "Executando build e subindo imagem para GCR privado":                 ***** END OF NOTICE *****
Step #0 - "Executando build e subindo imagem para GCR privado": 
Step #0 - "Executando build e subindo imagem para GCR privado": Sending build context to Docker daemon  6.656kB

Step #0 - "Executando build e subindo imagem para GCR privado": Step 1/6 : FROM golang:1.14.6-alpine
Step #0 - "Executando build e subindo imagem para GCR privado": 1.14.6-alpine: Pulling from library/golang
Step #0 - "Executando build e subindo imagem para GCR privado": Digest: sha256:d6deb50437547fd7226890aa19b075fbf7f5063e3c0d7a2eaf7fb41d11069013
Step #0 - "Executando build e subindo imagem para GCR privado": Status: Downloaded newer image for golang:1.14.6-alpine
Step #0 - "Executando build e subindo imagem para GCR privado":  ---> 30df784d6206
Step #0 - "Executando build e subindo imagem para GCR privado": Step 2/6 : RUN mkdir /go/src/soma
Step #0 - "Executando build e subindo imagem para GCR privado":  ---> Running in 092d188034e1
Step #0 - "Executando build e subindo imagem para GCR privado": Removing intermediate container 092d188034e1
Step #0 - "Executando build e subindo imagem para GCR privado":  ---> ae39ef68b8f3
Step #0 - "Executando build e subindo imagem para GCR privado": Step 3/6 : WORKDIR /go/src/soma
Step #0 - "Executando build e subindo imagem para GCR privado":  ---> Running in c22d98cc0cb4
Step #0 - "Executando build e subindo imagem para GCR privado": Removing intermediate container c22d98cc0cb4
Step #0 - "Executando build e subindo imagem para GCR privado":  ---> c93bef008003
Step #0 - "Executando build e subindo imagem para GCR privado": Step 4/6 : COPY ./soma.go ./soma_test.go ./
Step #0 - "Executando build e subindo imagem para GCR privado":  ---> 276c5a46eed9
Step #0 - "Executando build e subindo imagem para GCR privado": Step 5/6 : RUN go build soma.go
Step #0 - "Executando build e subindo imagem para GCR privado":  ---> Running in b003b9b26cb4
Step #0 - "Executando build e subindo imagem para GCR privado": Removing intermediate container b003b9b26cb4
Step #0 - "Executando build e subindo imagem para GCR privado":  ---> 0b2ed80c0281
Step #0 - "Executando build e subindo imagem para GCR privado": Step 6/6 : CMD ["./soma"]
Step #0 - "Executando build e subindo imagem para GCR privado":  ---> Running in ee73cd218465
Step #0 - "Executando build e subindo imagem para GCR privado": Removing intermediate container ee73cd218465
Step #0 - "Executando build e subindo imagem para GCR privado":  ---> 210bccfdbf7c
Step #0 - "Executando build e subindo imagem para GCR privado": Successfully built 210bccfdbf7c
Step #0 - "Executando build e subindo imagem para GCR privado": Successfully tagged gcr.io/codeeducation-test-285316/desafio-ci:latest
Step #0 - "Executando build e subindo imagem para GCR privado": Successfully tagged gcr.io/codeeducation-test-285316/desafio-ci:1.0.0
Finished Step #0 - "Executando build e subindo imagem para GCR privado"
Starting Step #1 - "Instalando o GO ..."
Step #1 - "Instalando o GO ...": Already have image (with digest): gcr.io/cloud-builders/go
Step #1 - "Instalando o GO ...": 
Step #1 - "Instalando o GO ...":                    ***** NOTICE *****
Step #1 - "Instalando o GO ...": 
Step #1 - "Instalando o GO ...": Alternative official `golang` images, including multiple versions across
Step #1 - "Instalando o GO ...": multiple platforms, are maintained by the Docker Community.
Step #1 - "Instalando o GO ...": 
Step #1 - "Instalando o GO ...": For details, visit https://hub.docker.com/_/golang.
Step #1 - "Instalando o GO ...": 
Step #1 - "Instalando o GO ...":                 ***** END OF NOTICE *****
Step #1 - "Instalando o GO ...": 
Step #1 - "Instalando o GO ...": Creating shadow workspace and symlinking source into "./gopath/src/soma".
Step #1 - "Instalando o GO ...": Documentation at https://github.com/GoogleCloudPlatform/cloud-builders/blob/master/go/README.md
Step #1 - "Instalando o GO ...": Binaries built using 'go install' will go to "/workspace/gopath/bin".
Step #1 - "Instalando o GO ...": Running: go install .
Finished Step #1 - "Instalando o GO ..."
Starting Step #2 - "Rodando testes ..."
Step #2 - "Rodando testes ...": Already have image (with digest): gcr.io/cloud-builders/go
Step #2 - "Rodando testes ...": 
Step #2 - "Rodando testes ...":                    ***** NOTICE *****
Step #2 - "Rodando testes ...": 
Step #2 - "Rodando testes ...": Alternative official `golang` images, including multiple versions across
Step #2 - "Rodando testes ...": multiple platforms, are maintained by the Docker Community.
Step #2 - "Rodando testes ...": 
Step #2 - "Rodando testes ...": For details, visit https://hub.docker.com/_/golang.
Step #2 - "Rodando testes ...": 
Step #2 - "Rodando testes ...":                 ***** END OF NOTICE *****
Step #2 - "Rodando testes ...": 
Step #2 - "Rodando testes ...": Creating shadow workspace and symlinking source into "./gopath/src/soma".
Step #2 - "Rodando testes ...":   File: './gopath/src/soma' -> '/workspace'
Step #2 - "Rodando testes ...":   Size: 10        	Blocks: 0          IO Block: 4096   symbolic link
Step #2 - "Rodando testes ...": Device: 801h/2049d	Inode: 1290256     Links: 1
Step #2 - "Rodando testes ...": Access: (0777/lrwxrwxrwx)  Uid: (    0/    root)   Gid: (    0/    root)
Step #2 - "Rodando testes ...": Access: 2020-08-06 00:35:15.000000000
Step #2 - "Rodando testes ...": Modify: 2020-08-06 00:35:15.000000000
Step #2 - "Rodando testes ...": Change: 2020-08-06 00:35:15.000000000
Step #2 - "Rodando testes ...": 
Step #2 - "Rodando testes ...": Documentation at https://github.com/GoogleCloudPlatform/cloud-builders/blob/master/go/README.md
Step #2 - "Rodando testes ...": Running: go test soma
Step #2 - "Rodando testes ...": ok  	soma	0.002s
Finished Step #2 - "Rodando testes ..."
Starting Step #3 - "Executando a funÃ§Ã£o soma."
Step #3 - "Executando a funÃ§Ã£o soma.": Already have image (with digest): gcr.io/cloud-builders/go
Step #3 - "Executando a funÃ§Ã£o soma.": 
Step #3 - "Executando a funÃ§Ã£o soma.":                    ***** NOTICE *****
Step #3 - "Executando a funÃ§Ã£o soma.": 
Step #3 - "Executando a funÃ§Ã£o soma.": Alternative official `golang` images, including multiple versions across
Step #3 - "Executando a funÃ§Ã£o soma.": multiple platforms, are maintained by the Docker Community.
Step #3 - "Executando a funÃ§Ã£o soma.": 
Step #3 - "Executando a funÃ§Ã£o soma.": For details, visit https://hub.docker.com/_/golang.
Step #3 - "Executando a funÃ§Ã£o soma.": 
Step #3 - "Executando a funÃ§Ã£o soma.":                 ***** END OF NOTICE *****
Step #3 - "Executando a funÃ§Ã£o soma.": 
Step #3 - "Executando a funÃ§Ã£o soma.": Creating shadow workspace and symlinking source into "./gopath/src/soma".
Step #3 - "Executando a funÃ§Ã£o soma.":   File: './gopath/src/soma' -> '/workspace'
Step #3 - "Executando a funÃ§Ã£o soma.":   Size: 10        	Blocks: 0          IO Block: 4096   symbolic link
Step #3 - "Executando a funÃ§Ã£o soma.": Device: 801h/2049d	Inode: 1290256     Links: 1
Step #3 - "Executando a funÃ§Ã£o soma.": Access: (0777/lrwxrwxrwx)  Uid: (    0/    root)   Gid: (    0/    root)
Step #3 - "Executando a funÃ§Ã£o soma.": Access: 2020-08-06 00:35:15.000000000
Step #3 - "Executando a funÃ§Ã£o soma.": Modify: 2020-08-06 00:35:15.000000000
Step #3 - "Executando a funÃ§Ã£o soma.": Change: 2020-08-06 00:35:15.000000000
Step #3 - "Executando a funÃ§Ã£o soma.": 
Step #3 - "Executando a funÃ§Ã£o soma.": Documentation at https://github.com/GoogleCloudPlatform/cloud-builders/blob/master/go/README.md
Step #3 - "Executando a funÃ§Ã£o soma.": Running: go run soma.go
Step #3 - "Executando a funÃ§Ã£o soma.": A soma de 5 + 5 Ã©: 10
Finished Step #3 - "Executando a funÃ§Ã£o soma."
PUSH
Pushing gcr.io/codeeducation-test-285316/desafio-ci:latest
The push refers to repository [gcr.io/codeeducation-test-285316/desafio-ci]
839499b6e33f: Preparing
ce8b05c2f9de: Preparing
ab60066b1646: Preparing
a31cd67316c2: Preparing
22690e5350e9: Preparing
1ba1431fe2ba: Preparing
0f7493e3a35b: Preparing
50644c29ef5a: Preparing
1ba1431fe2ba: Waiting
0f7493e3a35b: Waiting
50644c29ef5a: Waiting
22690e5350e9: Layer already exists
a31cd67316c2: Layer already exists
0f7493e3a35b: Layer already exists
1ba1431fe2ba: Layer already exists
50644c29ef5a: Layer already exists
ce8b05c2f9de: Pushed
ab60066b1646: Pushed
839499b6e33f: Pushed
latest: digest: sha256:d1dc4cecb85ca75edb546a8fc330455d5709f3cff0152b762f95118f6101895a size: 1990
Pushing gcr.io/codeeducation-test-285316/desafio-ci:1.0.0
The push refers to repository [gcr.io/codeeducation-test-285316/desafio-ci]
839499b6e33f: Preparing
ce8b05c2f9de: Preparing
ab60066b1646: Preparing
a31cd67316c2: Preparing
22690e5350e9: Preparing
1ba1431fe2ba: Preparing
0f7493e3a35b: Preparing
50644c29ef5a: Preparing
1ba1431fe2ba: Waiting
0f7493e3a35b: Waiting
50644c29ef5a: Waiting
a31cd67316c2: Layer already exists
22690e5350e9: Layer already exists
ce8b05c2f9de: Layer already exists
ab60066b1646: Layer already exists
839499b6e33f: Layer already exists
0f7493e3a35b: Layer already exists
50644c29ef5a: Layer already exists
1ba1431fe2ba: Layer already exists
1.0.0: digest: sha256:d1dc4cecb85ca75edb546a8fc330455d5709f3cff0152b762f95118f6101895a size: 1990
DONE
</code></pre>


