

<ins>Logging Practices Notes:<ins> 

I generally subscribe to the following convention:
Trace - Only when I would be "tracing" the code and trying to find one part of a function specifically.
Debug - Information that is diagnostically helpful to people more than just developers (IT, sysadmins, etc.).
Info - Generally useful information to log (service start/stop, configuration assumptions, etc). Info I want to always have available but usually don't care about under normal circumstances. This is my out-of-the-box config level.
Warn - Anything that can potentially cause application oddities, but for which I am automatically recovering. (Such as switching from a primary to backup server, retrying an operation, missing secondary data, etc.)
Error - Any error which is fatal to the operation, but not the service or application (can't open a required file, missing data, etc.). These errors will force user (administrator, or direct user) intervention. These are usually reserved (in my apps) for incorrect connection strings, missing services, etc.
Fatal - Any error that is forcing a shutdown of the service or application to prevent data loss (or further data loss). I reserve these only for the most heinous errors and situations where there is guaranteed to have been data corruption or loss.
 
From <https://stackoverflow.com/questions/2031163/when-to-use-the-different-log-levels>
 
 
Microsoft Doc - updated 5/9/2020:	https://docs.microsoft.com/en-us/aspnet/core/fundamentals/logging/?view=aspnetcore-3.1 
very detailed about all aspets
 
https://blog.rsuter.com/logging-with-ilogger-recommendations-and-best-practices/
 
 
 
=============================
Application Insights: - need to tune up on this - do not have much time today though
This article describes how to enable Application Insights for an ASP.NET Core application. 
https://docs.microsoft.com/en-us/azure/azure-monitor/app/asp-net-core
 
 
Adding to project ConstabularyFunctions: 
https://www.nuget.org/packages/Microsoft.ApplicationInsights.AspNetCore/2.8.2 
 
Creating an applicationinsights resource:
https://docs.microsoft.com/en-us/azure/azure-monitor/app/create-new-resource
 
 
Specifically about Monitoring Azure Functions:  https://docs.microsoft.com/en-us/azure/azure-functions/functions-monitoring?tabs=cmd 
Log Analytics  - https://docs.microsoft.com/en-us/azure/azure-functions/functions-monitor-log-analytics?tabs=csharp 
 
 
 
=============================
 
My implementation for having a convention i use everywhere.
it won't be the 'final' convention - rather call it draft 1.  We will evolve it.
Convention: 
<Status inside method>:  <ClassName.MethodName>  <list of parameters as key value pairs> return: <return value(s)> (return is optional)
 
Statuses:	Start,  End,  Error, 
Examples:
log.LogInformation($"Start: ProfileServiceUtility.IsValidOrganizationRole requestRoleId: {requestRoleId} organizationRoleIds: {orgIdsAsString}");
log.LogError(ex,$"Error: ProfileServiceUtility.IsValidOrganizationRole requestRoleId: {requestRoleId} organizationRoleIds: {orgIdsAsString}");
log.LogInformation($"End: ProfileServiceUtility.IsValidOrganizationRole requestRoleId: {requestRoleId} organizationRoleIds: {orgIdsAsString} return: {isValid}");
 
log.LogInformation($"Start: ProfileServiceUtility.GetProfile Oid: {oid}");
log.LogError(ex, $"Error: ProfileServiceUtility.GetProfile Oid: {oid}");
log.LogInformation($"End: ProfileServiceUtility.GetProfile Oid: {oid} return: {userProfile}");
 
 
 
Candidtes to have a Constants class of properties for various logging strings:
OK 200
 
BAD REQUEST 400
 
UNAUTHORIZED 401
 
NOT FOUND 404
 
INTERNAL SERVICE ERROR 500


