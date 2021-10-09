# assignment3
var c:String?
repeat
{
    print("----Pattern List----")
    print("1. Number right triangle")
    print("2. Sequential number right triangle")
    print("3. Pascal triangle")
    print("Enter your Choice : ")
    if let ch=Int(readLine()!)
    {
        switch(ch)
        {
          case 1:
                print("Enter number of rows: ")
                if let rows=Int(readLine()!)
                {
                  for i in 1...rows
                  {
                    for j in 1...i
                    {
                      print(j, terminator:" ")
                    }
                    print()
                  }
                }

            case 2: 
                print("Enter number of rows: ")
                if let rows=Int(readLine()!)
                {
                  var n=1
                  for i in 1...rows
                  {
                    for _ in 1...i
                    {
                      print(n, terminator:" ")
                      n=n+1
                    }
                    print()
                  }
                }

            case 3:
                var coef=1
                print("Enter number of rows: ")
                if let rows=Int(readLine()!)
                {
                  for i in 0...rows-1
                  {
                    for j in 0...i
                    {
                      if(j==0 || i==0)
                      {
                        coef=1
                      }
                      else
                      {
                        coef=coef*(i-j+1)/j
                      }
                      print(coef, terminator:" ")
                    }
                    print()
                  }
                }
                
            default:
                print("Wrong Choice")
      
        }
        print("Do You Want To Continue (y/n) ? ")
        c=readLine()!
    }
}
while(c=="y")
