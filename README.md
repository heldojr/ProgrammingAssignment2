# ProgrammingAssignment2
Caching the inverse of a matrix
## Put comments here that give an overall description of what your

1) cria a matriz (set), busca a matriz (get), criar a função do inverso (solvematrix) busca o inverso (getsolvematrix), armazena no cache (setsolveinverse)

## functions do

## Write a short comment describing this function

makeCacheMatrix <- function(x = matrix()) 

{solvematrix<-NULL

get<-function()x

set<-function(y) {

x<<-y

solvematrix<<-NULL}

getsolvematrix<-function()solvematrix

setsolvematrix<-function(inverse)

{solvematrix<<-inverse}

return(

list(set=set,get=get,getsolvematrix=getsolvematrix,setsolvematrix=solvematrix))

}

## Write a short comment describing this function

cacheSolve <- function(x, ...) {

inverse<-x$getsolvematrix()

if (!is.null(inverse))

{return(inverse)}

m<-solve(x$get())

x$setsolvematrix(m)

        ## Return a matrix that is the inverse of 'x'

}
