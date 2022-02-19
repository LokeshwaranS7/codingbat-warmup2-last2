*/"""Given a string, return the count of the number of times that a substring length 2 appears in the string and also as the last 2 chars of the string, so "hixxxhi" yields 1 (we won't count the end substring).
last2("hixxhi") → 1

last2("xaxxaxaxx") → 1

last2("axxxaaxx") → 2"""*/

//using while loop

	public int last2(String str) 
		{
		int h=0;
		int n=0;
		if (str.length()<2)
		{
  		return 0;
		}
		else
		{
    	String f=str.substring(str.length()-2,str.length());

		while(h<str.length()-2)
		{

  		if(str.substring(h,h+2).equals(f))
  		{
    		n+=1;
    		h+=1;
  		}
  		else
  		{
    		h+=1;
  		}
		}
		return n;

		}
	}
