---
title: Объект привязки к данным адресной книги
TOCTitle: Address Book Data-Binding object
ms:assetid: cf43f645-1ee1-8655-eb70-86d601e9f3f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250030(v=office.15)
ms:contentKeyID: 48547807
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fb5302d1c2b8e4eebb6dbe1a5906459834b8e41
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704303"
---
# <a name="address-book-data-binding-object"></a><span data-ttu-id="6d149-102">Объект привязки к данным адресной книги</span><span class="sxs-lookup"><span data-stu-id="6d149-102">Address Book Data-Binding object</span></span>


<span data-ttu-id="6d149-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d149-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d149-104">Приложение адресной книги использует [RDS. DataControl](datacontrol-object-rds.md) объект привязки данных из базы данных SQL Server к визуального объекта (в данном случае таблице DHTML) на странице HTML клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="6d149-104">The Address Book application uses the [RDS.DataControl](datacontrol-object-rds.md) object to bind data from the SQL Server database to a visual object (in this case, a DHTML table) in the application's client HTML page.</span></span> <span data-ttu-id="6d149-105">Логика программы VBScript событиями использует [RDS. DataControl](datacontrol-object-rds.md) для:</span><span class="sxs-lookup"><span data-stu-id="6d149-105">The event-driven VBScript program logic uses the [RDS.DataControl](datacontrol-object-rds.md) to:</span></span>

  - <span data-ttu-id="6d149-106">Запрос к базе данных, отправки обновлений в базу данных и обновить данные.</span><span class="sxs-lookup"><span data-stu-id="6d149-106">Query the database, send updates to the database, and refresh the data grid.</span></span>

  - <span data-ttu-id="6d149-107">Разрешить пользователям перемещение к первому, затем предыдущий, или последней записи в таблице данных.</span><span class="sxs-lookup"><span data-stu-id="6d149-107">Allow users to move to the first, next, previous, or last record in the data grid.</span></span>

<span data-ttu-id="6d149-108">В следующем коде определяется **RDS. DataControl** компонента:</span><span class="sxs-lookup"><span data-stu-id="6d149-108">The following code defines the **RDS.DataControl** component:</span></span>

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

<span data-ttu-id="6d149-109">Тег ОБЪЕКТА определяет **RDS. DataControl** компонента в программе.</span><span class="sxs-lookup"><span data-stu-id="6d149-109">The OBJECT tag defines the **RDS.DataControl** component in the program.</span></span> <span data-ttu-id="6d149-110">Тег включает два типа параметров:</span><span class="sxs-lookup"><span data-stu-id="6d149-110">The tag includes two types of parameters:</span></span>

  - <span data-ttu-id="6d149-111">Те, связанные с универсальный тег OBJECT.</span><span class="sxs-lookup"><span data-stu-id="6d149-111">Those associated with the generic OBJECT tag.</span></span>

  - <span data-ttu-id="6d149-112">Те, относящиеся к **RDS. DataControl** объекта.</span><span class="sxs-lookup"><span data-stu-id="6d149-112">Those specific to the **RDS.DataControl** object.</span></span>

## <a name="generic-object-tag-parameters"></a><span data-ttu-id="6d149-113">Универсальный объект тег параметров</span><span class="sxs-lookup"><span data-stu-id="6d149-113">Generic OBJECT Tag Parameters</span></span>

<span data-ttu-id="6d149-114">В следующей таблице описаны параметры, связанные с тег OBJECT.</span><span class="sxs-lookup"><span data-stu-id="6d149-114">The following table describes the parameters associated with the OBJECT tag.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d149-115">Параметр</span><span class="sxs-lookup"><span data-stu-id="6d149-115">Parameter</span></span></p></th>
<th><p><span data-ttu-id="6d149-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6d149-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d149-117"><strong><em>CLASSID</em></strong></span><span class="sxs-lookup"><span data-stu-id="6d149-117"><strong><em>CLASSID</em></strong></span></span></p></td>
<td><p><span data-ttu-id="6d149-118">Уникальный, 128-бит номер, идентифицирующий тип внедренный объект в систему.</span><span class="sxs-lookup"><span data-stu-id="6d149-118">A unique, 128-bit number that identifies the type of embedded object to the system.</span></span> <span data-ttu-id="6d149-119">Этот идентификатор сохраняется в локальном компьютере системного реестра.</span><span class="sxs-lookup"><span data-stu-id="6d149-119">This identifier is maintained in the local computer's system registry.</span></span> <span data-ttu-id="6d149-120">(Для класса идентификаторы <strong>RDS. DataControl</strong> , см <a href="datacontrol-object-rds.md">RDS. Объект DataControl</a>.)</span><span class="sxs-lookup"><span data-stu-id="6d149-120">(For the class IDs of the <strong>RDS.DataControl</strong> object, see <a href="datacontrol-object-rds.md">RDS.DataControl Object</a>.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d149-121"><strong><em>ID</em></strong></span><span class="sxs-lookup"><span data-stu-id="6d149-121"><strong><em>ID</em></strong></span></span></p></td>
<td><p><span data-ttu-id="6d149-122">Определяет идентификатор уровня документов для внедренный объект, используемый для идентификации в коде.</span><span class="sxs-lookup"><span data-stu-id="6d149-122">Defines a document-wide identifier for the embedded object that is used to identify it in code.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="rdsdatacontrol-tag-parameters"></a><span data-ttu-id="6d149-123">RDS. Параметры DataControl тег</span><span class="sxs-lookup"><span data-stu-id="6d149-123">RDS.DataControl Tag Parameters</span></span>

<span data-ttu-id="6d149-124">В следующей таблице описаны параметры, относящиеся к **RDS. DataControl** объекта.</span><span class="sxs-lookup"><span data-stu-id="6d149-124">The following table describes the parameters specific to the **RDS.DataControl** object.</span></span> <span data-ttu-id="6d149-125">(Чтобы получить полный список **RDS. DataControl** параметров объекта и способы их реализации, см [RDS. Объект DataControl](datacontrol-object-rds.md).)</span><span class="sxs-lookup"><span data-stu-id="6d149-125">(For a complete list of the **RDS.DataControl** object parameters, and when to implement them, see [RDS.DataControl object](datacontrol-object-rds.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d149-126">Параметр</span><span class="sxs-lookup"><span data-stu-id="6d149-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="6d149-127">Описание</span><span class="sxs-lookup"><span data-stu-id="6d149-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d149-128"><a href="server-property-rds.md">СЕРВЕР</a></span><span class="sxs-lookup"><span data-stu-id="6d149-128"><a href="server-property-rds.md">SERVER</a></span></span></p></td>
<td><p><span data-ttu-id="6d149-129">При использовании HTTP значение — это имя компьютера сервера, префикс https://.</span><span class="sxs-lookup"><span data-stu-id="6d149-129">If you are using HTTP, the value is the name of the server computer preceded by https:// .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d149-130"><a href="connect-property-rds.md">ПОДКЛЮЧЕНИЕ</a></span><span class="sxs-lookup"><span data-stu-id="6d149-130"><a href="connect-property-rds.md">CONNECT</a></span></span></p></td>
<td><p><span data-ttu-id="6d149-131">Предоставляет сведения о подключении, необходимые для <strong>RDS. DataControl</strong> для подключения к SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6d149-131">Provides the necessary connection information for the <strong>RDS.DataControl</strong> to connect to SQL Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d149-132"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado">SQL</a></span><span class="sxs-lookup"><span data-stu-id="6d149-132"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado">SQL</a></span></span></p></td>
<td><p><span data-ttu-id="6d149-133">Задает или возвращает строку запроса, используемое для извлечения <a href="recordset-object-ado.md">записей</a>.</span><span class="sxs-lookup"><span data-stu-id="6d149-133">Sets or returns the query string used to retrieve the <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
</tbody>
</table>

