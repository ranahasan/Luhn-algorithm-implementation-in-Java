# Luhn-algorithm-implementation-in-Java
```
public class LuhnAlg
{
        public static boolean Check(String ccNumber)
        {
                int total = 0;
                boolean alternateCheck = false;
                for (int i = ccNumber.length() - 1; i >= 0; i--)
                {
                        int n = Integer.parseInt(ccNumber.substring(i, i + 1));
                        if (alternateCheck)
                        {
                                n *= 2;
                                if (n > 9)
                                {
                                        n = (n % 10) + 1;
                                }
                        }
                        total += n;
                        alternateCheck = !alternateCheck;
                }
                return (total % 10 == 0);
        }
}
```
