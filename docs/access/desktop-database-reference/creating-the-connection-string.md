---
title: Создание строки подключения
TOCTitle: Creating the connection string
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f43207edec0c0acb58c66318e5dc7668a28ea595
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295329"
---
# <a name="creating-the-connection-string"></a><span data-ttu-id="d41cd-102">Создание строки подключения</span><span class="sxs-lookup"><span data-stu-id="d41cd-102">Creating the connection string</span></span>

<span data-ttu-id="d41cd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d41cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d41cd-104">ADO напрямую поддерживает пять аргументов в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="d41cd-104">ADO directly supports five arguments in a connection string.</span></span> <span data-ttu-id="d41cd-105">Другие аргументы передаются поставщику, указанному в аргументе *Поставщик*, без какой-либо обработки ADO.</span><span class="sxs-lookup"><span data-stu-id="d41cd-105">Other arguments are passed to the provider that is named in the *Provider* argument without any processing by ADO.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d41cd-106">Аргументация</span><span class="sxs-lookup"><span data-stu-id="d41cd-106">Argument</span></span></p></th>
<th><p><span data-ttu-id="d41cd-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d41cd-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d41cd-108"><em>Поставщик</em></span><span class="sxs-lookup"><span data-stu-id="d41cd-108"><em>Provider</em></span></span></p></td>
<td><p><span data-ttu-id="d41cd-109">Задает имя поставщика, чтобы использовать для подключения.</span><span class="sxs-lookup"><span data-stu-id="d41cd-109">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d41cd-110"><em>Имя файла</em></span><span class="sxs-lookup"><span data-stu-id="d41cd-110"><em>File Name</em></span></span></p></td>
<td><p><span data-ttu-id="d41cd-111">Указывает имя файла, соответствующего поставщику (например, исходный объект сохраненных данных), содержащий предварительно заданные сведения о подключении.</span><span class="sxs-lookup"><span data-stu-id="d41cd-111">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d41cd-112"><em>URL</em></span><span class="sxs-lookup"><span data-stu-id="d41cd-112"><em>URL</em></span></span></p></td>
<td><p><span data-ttu-id="d41cd-113">Указывает строку подключения как абсолютный URL-адрес, определяющий ресурс, например файл или папку.</span><span class="sxs-lookup"><span data-stu-id="d41cd-113">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d41cd-114"><em>Удаленный поставщик</em></span><span class="sxs-lookup"><span data-stu-id="d41cd-114"><em>Remote Provider</em></span></span></p></td>
<td><p><span data-ttu-id="d41cd-115">Указывает имя поставщика, используемого при открытии клиентского подключения.</span><span class="sxs-lookup"><span data-stu-id="d41cd-115">Specifies the name of a provider to use when opening a client-side connection.</span></span> <span data-ttu-id="d41cd-116">(Только служба удаленных данных.)</span><span class="sxs-lookup"><span data-stu-id="d41cd-116">(Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d41cd-117"><em>Удаленный сервер</em></span><span class="sxs-lookup"><span data-stu-id="d41cd-117"><em>Remote Server</em></span></span></p></td>
<td><p><span data-ttu-id="d41cd-118">Указывает путь к серверу, который будет применяться при открытии клиентского подключения.</span><span class="sxs-lookup"><span data-stu-id="d41cd-118">Specifies the path name of the server to use when opening a client-side connection.</span></span> <span data-ttu-id="d41cd-119">(Только служба удаленных данных.)</span><span class="sxs-lookup"><span data-stu-id="d41cd-119">(Remote Data Service only.)</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="d41cd-120">В следующих примерах и в руководстве программиста ADO для проверки подлинности на сервере используется код MyId с паролем "123aBc".</span><span class="sxs-lookup"><span data-stu-id="d41cd-120">In the following examples and throughout the ADO programmer's guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server.</span></span> <span data-ttu-id="d41cd-121">Эти значения следует заменить действительными учетными данными для входа на сервер.</span><span class="sxs-lookup"><span data-stu-id="d41cd-121">You should substitute these values with valid login credentials for your server.</span></span> <span data-ttu-id="d41cd-122">Кроме того, замените имя сервера на "MySqlServer".</span><span class="sxs-lookup"><span data-stu-id="d41cd-122">Also, substitute the name of your server for "MySqlServer".</span></span>

<span data-ttu-id="d41cd-123">Приложение HelloData в главе 1 использовало следующую строку подключения:</span><span class="sxs-lookup"><span data-stu-id="d41cd-123">The HelloData application in Chapter 1 used the following connection string:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="d41cd-124">Единственный параметр ADO, указанный в этой строке подключения, — "Provider=SQLOLEDB", который указал поставщика Microsoft OLE DB для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d41cd-124">The only ADO parameter supplied in this connection string was "Provider=SQLOLEDB", which indicated the Microsoft OLE DB Provider for SQL Server.</span></span> <span data-ttu-id="d41cd-125">Другие допустимые параметры, которые можно передать в строке подключения, могут определяться с помощью ссылки на документацию отдельных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="d41cd-125">Other valid parameters that can be passed in the connection string can be determined by referring to individual providers' documentation.</span></span> <span data-ttu-id="d41cd-126">Согласно поставщику OLE DB для SQL Server, можно заменить параметр  "Server" на параметр "Источник данных", а параметр "Database" на параметр *"Исходный каталог".*</span><span class="sxs-lookup"><span data-stu-id="d41cd-126">According to the OLE DB Provider for SQL Server documentation, you can substitute "Server" for the *Data Source* parameter and "Database" for the *Initial Catalog* parameter.</span></span> <span data-ttu-id="d41cd-127">Таким образом, следующая строка подключения дает результаты, идентичные первому:</span><span class="sxs-lookup"><span data-stu-id="d41cd-127">Thus, the following connection string would produce results identical to the first:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Server='MySqlServer';" & _ 
 "Database='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="d41cd-128">Чтобы открыть подключение, просто передав строку подключения в качестве первого аргумента в методе Open **объекта** **Connection:**</span><span class="sxs-lookup"><span data-stu-id="d41cd-128">To open the connection, simply pass the connection string as the first argument in the **Connection** object **Open** method:</span></span>

```vb 
 
objConn.Open m_sConnStr 
```

<span data-ttu-id="d41cd-129">Также можно указать большую часть подобных сведений, задав свойства объекта **Connection** перед открытием подключения.</span><span class="sxs-lookup"><span data-stu-id="d41cd-129">It is also possible to supply much of this information by setting properties of the **Connection** object before opening the connection.</span></span> <span data-ttu-id="d41cd-130">Например, можно добиться того же эффекта, что и в строке подключения выше, используя следующий код:</span><span class="sxs-lookup"><span data-stu-id="d41cd-130">For example, you could achieve the same effect as the connection string above by using the following code:</span></span>

```vb 
 
With objConn 
 .Provider = "SQLOLEDB" 
 .DefaultDatabase = "Northwind" 
 .Properties("Data Source") = "MySqlServer" 
 .Properties("Integrated Security") = "SSPI" 
 .Open 
End With 
```

