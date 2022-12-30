# Scoped
ASP.NET Core will create and share an instance of the service per request to the application. It means that a single instance of service is available per request. It will create a new instance in the new request. The service can be added as scoped using an AddScoped method of IServiceCollection. We need to take care while the service registered via Scoped in middleware and inject the service in the Invoke or InvokeAsync methods. If we inject dependency via the constructor, it behaves like a singleton object.
services.AddScoped<IHelloWorldService, HelloWorldService>();

