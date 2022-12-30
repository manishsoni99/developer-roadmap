# Scoped
ASP.NET Core will create and share a single instance of the service through the application life. The service can be added as a singleton using the AddSingleton method of IServiceCollection. ASP.NET Core creates a service instance at the time of registration and subsequence requests use this service instance. Here, we do not require to implement the Singleton design pattern and single instance maintained by the ASP.NET Core itself.
Example
services.AddSingleton<IHelloWorldService, HelloWorldService>();
