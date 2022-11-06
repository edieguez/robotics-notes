# Labels

- They follow the same [naming](../variables/naming.md) conventions as variables
- For readability, they are commonly expressed using uppercase letters with underscores between words
- Is possible to add optional labels to control and block statements, although is **highly uncommon**

``` java
// Labels in a loop
int[][] myComplexArray = {{5,2,1,3},{3,9,8,9},{5,7,12,7}};

OUTER_LOOP: for(int[] mySimpleArray : myComplexArray) {
    INNER_LOOP: for(int i=0; i<mySimpleArray.length; i++) {
        log.info(mySimpleArray[i]+"\t");
    }

    log.info("\n");
}

// Labels in a control sentence (if) and block statement. HIGHLY UNCOMMON
int frog = 15;

BAD_IDEA: if(frog>10)
    EVEN_WORSE_IDEA: {
    frog++;
}
```
