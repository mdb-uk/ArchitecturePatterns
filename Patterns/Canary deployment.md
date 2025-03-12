[[Architecture Patterns Index]] #Testing #Deployment
# Canary deployment

Rolling a change out to a small subset of users to minimise the chances of any issues.

There is a sub-technique called 1% Canary: a useful technique where we roll out new features to a very small segment (say 1%) of users carefully chosen across various user categories. This enables teams to capture fast user feedback, observe the impact of new releases on performance and stability and respond as necessary.


Before:
	![[Pasted image 20250131093201.png]]

After canary:
![[Pasted image 20250131093211.png]]

After full switch:
![[Pasted image 20250131093234.png]]

### References

[Canary Release](https://martinfowler.com/bliki/CanaryRelease.html)
