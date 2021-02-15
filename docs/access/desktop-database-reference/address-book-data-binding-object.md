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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281869"
---
# <a name="address-book-data-binding-object"></a><span data-ttu-id="3809f-102">Объект привязки к данным адресной книги</span><span class="sxs-lookup"><span data-stu-id="3809f-102">Address Book Data-Binding object</span></span>


<span data-ttu-id="3809f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3809f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3809f-104">Приложение адресной книги использует [RDS. Объект DataControl](datacontrol-object-rds.md) для привязки данных из базы данных SQL Server к визуальному объекту (в данном случае таблице DHTML) на HTML-странице клиента приложения.</span><span class="sxs-lookup"><span data-stu-id="3809f-104">The Address Book application uses the [RDS.DataControl](datacontrol-object-rds.md) object to bind data from the SQL Server database to a visual object (in this case, a DHTML table) in the application's client HTML page.</span></span> <span data-ttu-id="3809f-105">Программная логика VBScript на основе событий использует [RDS. DataControl для:](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="3809f-105">The event-driven VBScript program logic uses the [RDS.DataControl](datacontrol-object-rds.md) to:</span></span>

  - <span data-ttu-id="3809f-106">Запросите базу данных, отправьте обновления в базу данных и обновите сетку данных.</span><span class="sxs-lookup"><span data-stu-id="3809f-106">Query the database, send updates to the database, and refresh the data grid.</span></span>

  - <span data-ttu-id="3809f-107">Разрешить пользователям переходить к первой, следующей, предыдущей или последней записи в сетке данных.</span><span class="sxs-lookup"><span data-stu-id="3809f-107">Allow users to move to the first, next, previous, or last record in the data grid.</span></span>

<span data-ttu-id="3809f-108">Следующий код определяет **RDS. Компонент DataControl:**</span><span class="sxs-lookup"><span data-stu-id="3809f-108">The following code defines the **RDS.DataControl** component:</span></span>

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

<span data-ttu-id="3809f-109">Тег OBJECT определяет **RDS. Компонент DataControl** в программе.</span><span class="sxs-lookup"><span data-stu-id="3809f-109">The OBJECT tag defines the **RDS.DataControl** component in the program.</span></span> <span data-ttu-id="3809f-110">Тег включает два типа параметров:</span><span class="sxs-lookup"><span data-stu-id="3809f-110">The tag includes two types of parameters:</span></span>

  - <span data-ttu-id="3809f-111">Те, которые связаны с общим тегом OBJECT.</span><span class="sxs-lookup"><span data-stu-id="3809f-111">Those associated with the generic OBJECT tag.</span></span>

  - <span data-ttu-id="3809f-112">Те, которые специфиальна **для RDS. Объект DataControl.**</span><span class="sxs-lookup"><span data-stu-id="3809f-112">Those specific to the **RDS.DataControl** object.</span></span>

## <a name="generic-object-tag-parameters"></a><span data-ttu-id="3809f-113">Параметры generic OBJECT Tag</span><span class="sxs-lookup"><span data-stu-id="3809f-113">Generic OBJECT Tag Parameters</span></span>

<span data-ttu-id="3809f-114">В следующей таблице описываются параметры, связанные с тегом OBJECT.</span><span class="sxs-lookup"><span data-stu-id="3809f-114">The following table describes the parameters associated with the OBJECT tag.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3809f-115">Параметр</span><span class="sxs-lookup"><span data-stu-id="3809f-115">Parameter</span></span></p></th>
<th><p><span data-ttu-id="3809f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="3809f-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3809f-117"><strong><em>CLASSID</em></strong></span><span class="sxs-lookup"><span data-stu-id="3809f-117"><strong><em>CLASSID</em></strong></span></span></p></td>
<td><p><span data-ttu-id="3809f-118">Уникальный 128-битный номер, определяемый тип внедренного объекта в системе.</span><span class="sxs-lookup"><span data-stu-id="3809f-118">A unique, 128-bit number that identifies the type of embedded object to the system.</span></span> <span data-ttu-id="3809f-119">Этот идентификатор сохраняется в системный реестр локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="3809f-119">This identifier is maintained in the local computer's system registry.</span></span> <span data-ttu-id="3809f-120">(Для ИД класса <strong>RDS. Объект DataControl</strong> см. в <a href="datacontrol-object-rds.md">RDS. Объект DataControl.)</a></span><span class="sxs-lookup"><span data-stu-id="3809f-120">(For the class IDs of the <strong>RDS.DataControl</strong> object, see <a href="datacontrol-object-rds.md">RDS.DataControl Object</a>.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3809f-121"><strong><em>ID</em></strong></span><span class="sxs-lookup"><span data-stu-id="3809f-121"><strong><em>ID</em></strong></span></span></p></td>
<td><p><span data-ttu-id="3809f-122">Определяет идентификатор для всего документа для внедренного объекта, который используется для его идентификации в коде.</span><span class="sxs-lookup"><span data-stu-id="3809f-122">Defines a document-wide identifier for the embedded object that is used to identify it in code.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="rdsdatacontrol-tag-parameters"></a><span data-ttu-id="3809f-123">RDS. Параметры тега DataControl</span><span class="sxs-lookup"><span data-stu-id="3809f-123">RDS.DataControl Tag Parameters</span></span>

<span data-ttu-id="3809f-124">В следующей таблице описываются параметры, специфические для **RDS. Объект DataControl.**</span><span class="sxs-lookup"><span data-stu-id="3809f-124">The following table describes the parameters specific to the **RDS.DataControl** object.</span></span> <span data-ttu-id="3809f-125">(Полный список **RDS. Параметры объекта DataControl** и время их реализации см. в [RDS. Объект DataControl.)](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="3809f-125">(For a complete list of the **RDS.DataControl** object parameters, and when to implement them, see [RDS.DataControl object](datacontrol-object-rds.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3809f-126">Параметр</span><span class="sxs-lookup"><span data-stu-id="3809f-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="3809f-127">Описание</span><span class="sxs-lookup"><span data-stu-id="3809f-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3809f-128"><a href="server-property-rds.md">SERVER</a></span><span class="sxs-lookup"><span data-stu-id="3809f-128"><a href="server-property-rds.md">SERVER</a></span></span></p></td>
<td><p><span data-ttu-id="3809f-129">Если используется ПРОТОКОЛ HTTP, значением будет имя сервера, предшествующего https://.</span><span class="sxs-lookup"><span data-stu-id="3809f-129">If you are using HTTP, the value is the name of the server computer preceded by https:// .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3809f-130"><a href="connect-property-rds.md">CONNECT</a></span><span class="sxs-lookup"><span data-stu-id="3809f-130"><a href="connect-property-rds.md">CONNECT</a></span></span></p></td>
<td><p><span data-ttu-id="3809f-131">Предоставляет необходимые сведения о под соединении <strong>для RDS. DataControl</strong> для подключения к SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3809f-131">Provides the necessary connection information for the <strong>RDS.DataControl</strong> to connect to SQL Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3809f-132"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado">SQL</a></span><span class="sxs-lookup"><span data-stu-id="3809f-132"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado">SQL</a></span></span></p></td>
<td><p><span data-ttu-id="3809f-133">Задает или возвращает строку запроса, используемую для извлечения <a href="recordset-object-ado.md">набора записей.</a></span><span class="sxs-lookup"><span data-stu-id="3809f-133">Sets or returns the query string used to retrieve the <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
</tbody>
</table>

