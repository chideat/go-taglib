taglib.go
=========

Interface to the taglib audio tagging library with Apache license.

Example
-------

    package main

    import "bitbucket.org/taruti/taglib.go"
    import "fmt"

    func main() {
        f := taglib.Open("foo.mp3")
        if f==nil { return }
        defer f.Close()
        fmt.Printf("%v\n",f.GetTags())
        fmt.Printf("%v\n",f.GetProperties())
    }
