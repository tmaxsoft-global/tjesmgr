Using Tjesmgr JCL SCAN
======================

-   Execution

-   Result Verification

Here is our test JCL:

<img src="./media/image1.png" style="width:6.17708in;height:4.64583in" />

Executing the JCL SCAN Command (JEM)
------------------------------------

> tjesmgr jem &lt;JOBNAME&gt;

Ex.

<img src="./media/image2.png" style="width:6.5in;height:0.66597in" />

Checking Results from JCL SCAN 
-------------------------------

This process is the same for checking any JOB. The JCL was not run
during the JCL SCAN, but a JOB was submitted to do syntax checking and
dataset checks to see if any were already catalogued.

Therefore, we can use the same commands as if checking any other job

> tjesmgr psj &lt;JOBID&gt;

<img src="./media/image3.png" style="width:6.5in;height:4.17639in" />

Here, we can check the SYSMSG for any syntax related issues, or Dataset
issues.

While in tjesmgr …

> podd @j di=1
>
> or
>
> podd &lt;JOBID&gt; di=1

<img src="./media/image4.png" style="width:6.5in;height:1.94306in" />
