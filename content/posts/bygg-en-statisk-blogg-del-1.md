+++
date = "2019-05-05T17:44:03+02:00"
draft = false
frontimage = "https://picsum.photos/1920/300?q=83594583949839"
summary = "Enkel blogg med hugo"
title = "Bygg en statisk blogg - Del 1"

+++


{{< highlight go "linenos=table,hl_lines=8 15-17,linenostart=1" >}}
// _Functions_ are central in Go. We'll learn about
// functions with a few different examples.

package main

import "fmt"

// Here's a function that takes two `int`s and returns
// their sum as an `int`.
func plus(a int, b int) int {

    // Go requires explicit returns, i.e. it won't
    // automatically return the value of the last
    // expression.
    return a + b
}

// When you have multiple consecutive parameters of
// the same type, you may omit the type name for the
// like-typed parameters up to the final parameter that
// declares the type.
func plusPlus(a, b, c int) int {
    return a + b + c
}

func main() {

    // Call a function just as you'd expect, with
    // `name(args)`.
    res := plus(1, 2)
    fmt.Println("1+2 =", res)

    res = plusPlus(1, 2, 3)
    fmt.Println("1+2+3 =", res)
}

{{< / highlight >}}


Lorem ipsum dolor sit amet, consectetur adipiscing elit. In tellus nibh, aliquam eu leo eget, pretium rhoncus eros. Vivamus consectetur arcu vitae dui molestie egestas ut ac risus. In commodo metus id purus varius, sit amet varius velit efficitur. Aliquam convallis ante vitae vulputate venenatis. Maecenas eleifend metus at luctus convallis. Curabitur rhoncus hendrerit elit id dapibus. Sed quis viverra magna. Cras tincidunt dignissim pulvinar. Quisque augue felis, aliquet at congue vel, viverra ac ante. Proin euismod neque risus, eget varius ex porta non. Nullam at tortor condimentum massa suscipit molestie. Aenean imperdiet eu dui eget condimentum. Nulla semper condimentum hendrerit. Aenean eleifend nisl tellus, et auctor metus dignissim at. Sed sit amet erat lectus.