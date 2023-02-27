# Microservices 
	Small Autonomous services
	Deployed separately
	Loosely Coupled and focused on a single task
	
## Advantages
	Tech Heterogeneity
	Resilience
	Scaling
	Easy Deployments
	Organization
	
## Disadvantages
	Inter services Communication
		Handle exceptions/Timeouts from other services
		Retries
		Circuit breaking
	Distributed Transactions
		Two Phase commit
		Saga
	More Resources
		For deployment
	Debugging Issues
		Distributed tracing
		Distributed logging
	Maintenance
	
# Monoliths
	Single Application having all the services
	Example 
		Ecommerce App -> 
			Inventory, 
			Order, 
			Payment & Billings, 
			Delivery, 
			User Managements
		
## Advantages	
	Simple 
		Develop
		Deploy
		Scale
		
## Disadvantages
	Tech Dependencies
	Scaling Individual services is not possible
	Large Deployments
		Risky
		Slow build/Test
	
# Domain Driven Design

## Domain 
	Example Ecommerce

## Bounded Context
	Example Warehouse

## Shared Context
	Example Stock
	
* Different model may have different meanings in different context * 
**Loose Coupling**
	A change in one service should not require a change in another
	
**High Cohesion**
	We should group related services together and unrelated services should be grouped separately


# What causes Tight coulping?
	Integration
	Chatty Services
	
# Functional Decomposition
	Breaking existing monliths into smaller microservices
	
	
	