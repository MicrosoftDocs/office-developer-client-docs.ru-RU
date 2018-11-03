---
title: Создание строки подключения
TOCTitle: Creating the Connection String
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b346cd5c53ee101809237896acc0806bbf4e4624
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936933"
---
# <a name="creating-the-connection-string"></a><span data-ttu-id="e2efa-102">Создание строки подключения</span><span class="sxs-lookup"><span data-stu-id="e2efa-102">Creating the Connection String</span></span>


<span data-ttu-id="e2efa-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2efa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e2efa-104">ADO поддерживает пять аргументов в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="e2efa-104">ADO directly supports five arguments in a connection string.</span></span> <span data-ttu-id="e2efa-105">Другие аргументы передаются поставщика с именем в аргументе *поставщика* без какой-либо обработки с ADO.</span><span class="sxs-lookup"><span data-stu-id="e2efa-105">Other arguments are passed to the provider that is named in the *Provider* argument without any processing by ADO.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2efa-106">Аргумент</span><span class="sxs-lookup"><span data-stu-id="e2efa-106">Argument</span></span></p></th>
<th><p><span data-ttu-id="e2efa-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e2efa-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2efa-108"><em>Поставщик</em></span><span class="sxs-lookup"><span data-stu-id="e2efa-108"><em>Provider</em></span></span></p></td>
<td><p><span data-ttu-id="e2efa-109">Задает имя поставщика, который используется для подключения.</span><span class="sxs-lookup"><span data-stu-id="e2efa-109">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2efa-110"><em>Имя файла</em></span><span class="sxs-lookup"><span data-stu-id="e2efa-110"><em>File Name</em></span></span></p></td>
<td><p><span data-ttu-id="e2efa-111">Указывает имя файла от поставщика (например, объект источника постоянных данных), содержащий сведения о подключении к предварительно.</span><span class="sxs-lookup"><span data-stu-id="e2efa-111">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2efa-112"><em>URL</em>.</span><span class="sxs-lookup"><span data-stu-id="e2efa-112"><em>URL</em></span></span></p></td>
<td><p><span data-ttu-id="e2efa-113">Указывает строку подключения, как абсолютный URL-адрес, идентифицирующий ресурс, такой как файл или папку.</span><span class="sxs-lookup"><span data-stu-id="e2efa-113">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2efa-114"><em>Удаленный поставщик</em></span><span class="sxs-lookup"><span data-stu-id="e2efa-114"><em>Remote Provider</em></span></span></p></td>
<td><p><span data-ttu-id="e2efa-115">Задает имя поставщика для использования при открытии подключения со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="e2efa-115">Specifies the name of a provider to use when opening a client-side connection.</span></span> <span data-ttu-id="e2efa-116">(Служба удаленных данных только.)</span><span class="sxs-lookup"><span data-stu-id="e2efa-116">(Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2efa-117"><em>Удаленный сервер</em></span><span class="sxs-lookup"><span data-stu-id="e2efa-117"><em>Remote Server</em></span></span></p></td>
<td><p><span data-ttu-id="e2efa-118">Задает имя пути сервера, который будет использоваться при открытии подключения со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="e2efa-118">Specifies the path name of the server to use when opening a client-side connection.</span></span> <span data-ttu-id="e2efa-119">(Служба удаленных данных только.)</span><span class="sxs-lookup"><span data-stu-id="e2efa-119">(Remote Data Service only.)</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="e2efa-120">В следующих примерах и во всем Руководство программиста ADO идентификатор пользователя «Мой_идентификатор» пароль «123aBc» используется для проверки подлинности на сервере.</span><span class="sxs-lookup"><span data-stu-id="e2efa-120">In the following examples and throughout the ADO programmer's guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server.</span></span> <span data-ttu-id="e2efa-121">Необходимо заменить эти значения с действительные учетные данные для сервера.</span><span class="sxs-lookup"><span data-stu-id="e2efa-121">You should substitute these values with valid login credentials for your server.</span></span> <span data-ttu-id="e2efa-122">Кроме того замените имя сервера для «MySqlServer».</span><span class="sxs-lookup"><span data-stu-id="e2efa-122">Also, substitute the name of your server for "MySqlServer".</span></span>

<span data-ttu-id="e2efa-123">В приложении HelloData в раздел 1 используется следующая строка подключения:</span><span class="sxs-lookup"><span data-stu-id="e2efa-123">The HelloData application in Chapter 1 used the following connection string:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="e2efa-124">Единственный параметр ADO, предоставленные в этой строке подключения был «поставщика = SQLOLEDB», который указан поставщик Microsoft OLE DB для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e2efa-124">The only ADO parameter supplied in this connection string was "Provider=SQLOLEDB", which indicated the Microsoft OLE DB Provider for SQL Server.</span></span> <span data-ttu-id="e2efa-125">Другие допустимые параметры, которые могут быть переданы в строке подключения можно определить, обратившись к документации отдельные поставщики.</span><span class="sxs-lookup"><span data-stu-id="e2efa-125">Other valid parameters that can be passed in the connection string can be determined by referring to individual providers' documentation.</span></span> <span data-ttu-id="e2efa-126">В соответствии с поставщика OLE DB для документации по SQL Server можно заменить «Сервер» для параметра *Источник данных* и «База данных» для параметра *Initial Catalog* .</span><span class="sxs-lookup"><span data-stu-id="e2efa-126">According to the OLE DB Provider for SQL Server documentation, you can substitute "Server" for the *Data Source* parameter and "Database" for the *Initial Catalog* parameter.</span></span> <span data-ttu-id="e2efa-127">Таким образом следующая строка подключения может привести к результатам совпадает с первым:</span><span class="sxs-lookup"><span data-stu-id="e2efa-127">Thus, the following connection string would produce results identical to the first:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Server='MySqlServer';" & _ 
 "Database='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="e2efa-128">Для открытия подключения, просто передайте строку подключения в качестве первого аргумента в метод **Open** объекта **подключения** :</span><span class="sxs-lookup"><span data-stu-id="e2efa-128">To open the connection, simply pass the connection string as the first argument in the **Connection** object **Open** method:</span></span>

```vb 
 
objConn.Open m_sConnStr 
```

<span data-ttu-id="e2efa-129">Можно также предоставить большую часть этих сведений путем установки свойства объекта **подключения** перед открытием подключения.</span><span class="sxs-lookup"><span data-stu-id="e2efa-129">It is also possible to supply much of this information by setting properties of the **Connection** object before opening the connection.</span></span> <span data-ttu-id="e2efa-130">Например можно получить же эффект, что строка подключения выше, с помощью следующего кода:</span><span class="sxs-lookup"><span data-stu-id="e2efa-130">For example, you could achieve the same effect as the connection string above by using the following code:</span></span>

```vb 
 
With objConn 
 .Provider = "SQLOLEDB" 
 .DefaultDatabase = "Northwind" 
 .Properties("Data Source") = "MySqlServer" 
 .Properties("Integrated Security") = "SSPI" 
 .Open 
End With 
```

