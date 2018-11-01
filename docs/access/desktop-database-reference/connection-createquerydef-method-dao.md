---
title: Connection.CreateQueryDef Method (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 254fe81a-9b45-e8e7-108d-503c1c1c0fcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191860(v=office.15)
ms:contentKeyID: 48543781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053067
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5ea0e06d133c95506a68e947254bfcd0ea8a2dc6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880308"
---
# <a name="connectioncreatequerydef-method-dao"></a><span data-ttu-id="a413a-102">Connection.CreateQueryDef Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="a413a-102">Connection.CreateQueryDef Method (DAO)</span></span>


<span data-ttu-id="a413a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a413a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a413a-104">Создает новый объект **[QueryDef](querydef-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="a413a-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a413a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a413a-105">Syntax</span></span>

<span data-ttu-id="a413a-106">*выражение* . CreateQueryDef (***имя***, ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="a413a-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="a413a-107">*выражение* Переменная, которая содержит объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="a413a-107">*expression* A variable that represents a **Connection** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="a413a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a413a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a413a-109">Имя</span><span class="sxs-lookup"><span data-stu-id="a413a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a413a-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="a413a-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="a413a-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a413a-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="a413a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a413a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a413a-113">Имя</span><span class="sxs-lookup"><span data-stu-id="a413a-113">Name</span></span></p></td>
<td><p><span data-ttu-id="a413a-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="a413a-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="a413a-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a413a-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a413a-116"><strong>Variant</strong> (<strong>String</strong> подтип), уникальным образом новые <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="a413a-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a413a-117">SQLText</span><span class="sxs-lookup"><span data-stu-id="a413a-117">SQLText</span></span></p></td>
<td><p><span data-ttu-id="a413a-118">Необязательный</span><span class="sxs-lookup"><span data-stu-id="a413a-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="a413a-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a413a-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a413a-120"><strong>Variant</strong> (<strong>String</strong> подтип), которая является инструкцией SQL, определение <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="a413a-120">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>.</span></span> <span data-ttu-id="a413a-121">Если опустить аргумент, можно определить <strong>QueryDef</strong> путем установки свойства <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> до или после добавления его в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="a413a-121">If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a413a-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a413a-122">Return value</span></span>

<span data-ttu-id="a413a-123">QueryDef</span><span class="sxs-lookup"><span data-stu-id="a413a-123">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="a413a-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="a413a-124">Remarks</span></span>

<span data-ttu-id="a413a-125">В рабочей области Microsoft Access Если вы укажите отличное от строку нулевой длины имени при создании **QueryDef**результирующего объекта **QueryDef** автоматически добавляется к коллекции **[QueryDefs](querydefs-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="a413a-125">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="a413a-126">Если объектом, заданным с именем уже должна быть членом **QueryDefs** коллекции, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="a413a-126">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="a413a-127">Временные **QueryDef** можно создать с помощью строку нулевой длины для аргумента имени, при выполнении метода **CreateQueryDef** .</span><span class="sxs-lookup"><span data-stu-id="a413a-127">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="a413a-128">Это также можно сделать, задав свойство **[Name](connection-name-property-dao.md)** только что созданный **QueryDef** в строку нулевой длины (»»).</span><span class="sxs-lookup"><span data-stu-id="a413a-128">You can also accomplish this by setting the **[Name](connection-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> <span data-ttu-id="a413a-129">Временные объекты **QueryDef** полезны, если требуется повторно использовать динамические инструкции SQL, не создавая для создания новых постоянных объектов в коллекции **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="a413a-129">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="a413a-130">Временные **QueryDef** невозможно добавить в любой коллекции, так как строку нулевой длины не является допустимым именем для постоянного объекта **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="a413a-130">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="a413a-131">Всегда можно задать **имя** и свойства **SQL** объекта **QueryDef** только что созданный и затем добавьте **QueryDef** в коллекцию **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="a413a-131">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="a413a-132">Чтобы запустить инструкции SQL в объект **QueryDef** , используйте метод **[Execute](connection-execute-method-dao.md)** или **[OpenRecordset](connection-openrecordset-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="a413a-132">To run the SQL statement in a **QueryDef** object, use the **[Execute](connection-execute-method-dao.md)** or **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="a413a-133">С помощью объекта **QueryDef** является предпочтительным для выполнения запросов к серверу с использованием баз данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="a413a-133">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="a413a-134">Для удаления объекта **QueryDef** из коллекции **QueryDefs** в базе данных ядра базы данных Microsoft Access, используйте метод **[Delete](fields-delete-method-dao.md)** в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="a413a-134">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

