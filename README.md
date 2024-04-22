# 13.ACE-SwitchArrow  
Listing 13 ACE-SwitchArrow/SwitchArrow.java Page 34  
  
Starting from Java 14, instead of the colon, one can use the “arrow”, i.e., the two-character ’->’ symbol (but one cannot mix colons and arrows in one switch statement).  
Then  
  • the “fall through” feature is “turned off”;  
  • to the right of the arrow, one can only use:  
    1. single statement or expression,  
    2. a block (enclosed in braces),  
    3. a throw statement.  
  
For example in the following example (Listing 13), we don’t use any break statements.
