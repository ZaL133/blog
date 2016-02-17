<!DOCTYPE html>
<html>
        <h1>Redirect</h1>
        <p class="description">
            I can never remember which method to return for an MVC redirect.
            <ul>
                <li><a href="#redirect">Redirect</a></li>
                <li><a href="#redirectPerm">RedirectPermanent</a></li>
                <li><a href="#redirectAction">RedirectToAction, RedirectToActionPermanent</a></li>
                <li><a href="#redirectRoute">RedirectToRoute, RedirectToRoutePermanent</a></li>
                <li><a href="#transfer">Transfer, TransferRequest</a></li>
            </ul>
        </p>
        <div>
            The main differences between the base and the *Permantent are the <code>Redirect</code> will return a <a href="https://en.wikipedia.org/wiki/HTTP_302">302 (found)</a>, while the <code>RedirectPermanent</code> will return a <a href="https://en.wikipedia.org/wiki/HTTP_301">301 (Moved Permantently) </a>
        </div>
        
        <div id="redirect" class="section">
            <h2>Redirect</h2>
            Returns a 302 (Found) to the given url
            <div>
                <img src="RedirMethod.png" alt="Redirect Method" />
            </div>
            <div>
                <img src="RedirHeaders.png" alt="Redirect Headers" />
            </div>
        </div>
        
        <div id="redirectPerm" class="section">
            <h2>Redirect Permanent</h2>
            Returns a 301 (Moved Permanently) to the given url
            <div>
                <img src="RedirPermMethod.png" alt="Redirect Permanent Method" />
            </div>
            <div>
                <img src="RedirPermHeaders.png" alt="Redirect Permanent Headers" />
            </div>
        </div>
        
        <div id="redirectAction">
            <h2>RedirectToAction, RedirectToActionPermanent</h2>
            <p>These work the same as the Redirect(Permanent) methods, but are formed MVC-ish in that you specify the action, controller, and model as you would using the <code>@Url.Action</code> helper method or <code>@Html.ActionLink</code>
            <div>
                <img src="RedirActionMethod.png" alt="Redirect Permanent Method" />
            </div>
            <div>
                <img src="RedirActionHeaders.png" alt="Redirect Permanent Headers" />
            </div>            
        </div>
        
        <div id="redirectRoute">
            <h2>RedirectToRoute, RedirectToRoutePermanent</h2>
            <p>These methods allow you to specify the route name (as specified in your RouteConfig.cs and stored in your <a href="https://msdn.microsoft.com/en-us/library/system.web.routing.routetable.routes.aspx">RouteTable</a> ) & values rather than the Action/Controller values.  </p>
            <div>
                <img src="RedirRouteMethod.png" alt="Redirect Permanent Method" />
            </div>
            <div>
                <img src="RedirRouteHeaders.png" alt="Redirect Permanent Headers" />
            </div>            
        </div>
        
        <div id="transfer" class="section">
            <h2>Transfer, TransferRequest</h2>
            <p>These can be used to execute a different url and return the results<br>
            <code>Transfer</code> is used in < IIS7<br>
            <code>TransferRequest</code> is used in <a href="http://www.iis.net/learn/application-frameworks/building-and-running-aspnet-applications/how-to-take-advantage-of-the-iis-integrated-pipeline">Integrated Pipeline Mode</a>
            </p>
            <div>
                <img src="TransferRequestMethod.png" alt="Transfer Request Method" />
            </div>
            <div>
                <img src="TransferRequestHeaders.png" alt="Transfer Request Headers" />
            </div>                
        </div>
</html>