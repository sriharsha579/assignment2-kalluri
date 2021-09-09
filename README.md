# assignment2-kalluri

# shanmukha sriharsha kalluri

###### alaska

**alaska** was a city to visit atleast once in **lifetime** 


---

Directions from Maryville to alaska 

 1. Book a flight ticket for flying
     * go on time to the airport
 2. Take a sleep for a long flight 
     * have a peaceful sleep for 10hrs
 3. Book a taxi in alaska  
     * 3.1 list out the places to visit with local map
     * 3.2 And start exploring the alaska city 

---

List of items to be brought alaska for maximum enjoyment

* Get some local guys over there
* to build up some memories bring the items like 
  * camera
  * tripod
  * go pro
* places to be visited in alaska 
   * Denali National park and reserve 
   * Hubbard Glacier
   * Kenai Fjords National park

   ---

   ## You may know me here ##


   [Bio and image](aboutme.md)  

   ---

   ### food i would recommend others ###

   |  food  |   place  |  price   |
   |--------|----------|----------|
   |maharaja burger|Mc Donalds| $1.79|
   |pagalial's pizza buffet|pagalial's pizza| $13.69|
   |cheese pizza|dominos| $4.23|
   |12 pc wings|KFC|$16.72|

   ---

   ## Pithy Quotes ##
    Once you replace **negative** thoughts with **positive** ones, you'll start having **positive** results. - *Willi Neilson*

    Two things are **infinite**: the **universe** and human **stupidity**; and I'm not sure about the universe. - *Albert Einisten*

    ---
    
    ## code fencing ##

    In systems theory, a linear system is a **mathematical model** of a system based on the use of a "linear operator". Linear systems typically exhibit features and properties that are much simpler than the **nonlinear case**. As a mathematical abstraction or idealization, **linear systems** find important applications in automatic control theory,**signal processing**, and **telecommunications**. For example, the propagation medium for wireless communication systems can often be modeled by linear systems.

    ### link for the description ###

    [description of linear systems](https://en.wikipedia.org/wiki/Linear_system)

    ```

    const double EPS = 1e-9;
const int INF = 2; // it doesn't actually have to be infinity or a big number

int gauss (vector < vector<double> > a, vector<double> & ans) {
    int n = (int) a.size();
    int m = (int) a[0].size() - 1;

    vector<int> where (m, -1);
    for (int col=0, row=0; col<m && row<n; ++col) {
        int sel = row;
        for (int i=row; i<n; ++i)
            if (abs (a[i][col]) > abs (a[sel][col]))
                sel = i;
        if (abs (a[sel][col]) < EPS)
            continue;
        for (int i=col; i<=m; ++i)
            swap (a[sel][i], a[row][i]);
        where[col] = row;

        for (int i=0; i<n; ++i)
            if (i != row) {
                double c = a[i][col] / a[row][col];
                for (int j=col; j<=m; ++j)
                    a[i][j] -= a[row][j] * c;
            }
        ++row;
    }

    ans.assign (m, 0);
    for (int i=0; i<m; ++i)
        if (where[i] != -1)
            ans[i] = a[where[i]][m] / a[where[i]][i];
    for (int i=0; i<n; ++i) {
        double sum = 0;
        for (int j=0; j<m; ++j)
            sum += ans[j] * a[i][j];
        if (abs (sum - a[i][m]) > EPS)
            return 0;
    }

    for (int i=0; i<m; ++i)
        if (where[i] == -1)
            return INF;
    return 1;
}

```

### Code Source ###

[Link to the Source](https://cp-algorithms.com/linear_algebra/linear-system-gauss.html)


