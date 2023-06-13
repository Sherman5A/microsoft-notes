
# Resource Locks

Resource locks,
> Prevent resources from being accidentally deleted or changed

Even with RBAC, there is still a risk of deletion of critical cloud resources.

Resource locks can be applied to any scopes in the hierarchy. Furthermore, they are inherited.

Resource locks have 2 types,
- Delete - **Users can still read and modify resources, but they can not delete it**
- ReadOnly - **Users can read a resource, but can not update or delete the resources**

