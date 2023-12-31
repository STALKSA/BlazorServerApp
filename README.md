# Blazor

Blazor — это веб-платформа для создания компонентов веб-интерфейса ( компоненты Razor ), которые можно размещать различными способами. Компоненты Razor могут выполняться на стороне сервера в ASP.NET Core ( Blazor Server ), а не на стороне клиента в браузере в среде выполнения .NET на основе WebAssembly ( Blazor WebAssembly , Blazor WASM ).  Больше информации на [официальном Сайте Blazor](https://dotnet.microsoft.com/en-us/apps/aspnet/web-apps/blazor).

## Blazor Server

В модели размещения Blazor Server приложение выполняется на сервере из приложения ASP.NET Core. Обновления пользовательского интерфейса, обработка событий и вызовы JavaScript обрабатываются через подключение SignalR с использованием протокола WebSockets . Состояние на сервере, связанное с каждым подключенным клиентом, называется схемой . Цепи не привязаны к конкретному сетевому соединению и могут допускать временные сбои в сети и попытки клиента повторно подключиться к серверу при потере соединения.

В приложении Blazor Server для каждого экрана браузера требуется отдельная схема и отдельные экземпляры состояния компонента, управляемого сервером. Blazor считает закрытие вкладки браузера или переход по внешнему URL-адресу изящным завершением. В случае корректного завершения цепь и связанные с ней ресурсы немедленно освобождаются. Клиент также может отключиться некорректно, например, из-за сбоя в сети. Blazor Server сохраняет отключенные каналы в течение настраиваемого интервала времени, чтобы клиент мог повторно подключиться.


![Пример](https://learn.microsoft.com/en-us/aspnet/core/blazor/hosting-models/_static/blazor-server.png?view=aspnetcore-7.0)

1. Реализовать красивый вывод товаров из каталога (например, через table).
2. На главное странице реализовать вывод "живого" времени.
