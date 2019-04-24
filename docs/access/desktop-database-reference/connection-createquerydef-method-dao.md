---
title: Метод Connection. CreateQueryDef (DAO)
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
localization_priority: Normal
ms.openlocfilehash: b6600d4508a33a31098d6a2e7c92f5904beb0e95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295935"
---
# <a name="connectioncreatequerydef-method-dao"></a><span data-ttu-id="10243-102">Метод Connection. CreateQueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="10243-102">Connection.CreateQueryDef method (DAO)</span></span>

<span data-ttu-id="10243-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="10243-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="10243-104">Создает новый объект **[QueryDef](querydef-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="10243-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="10243-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10243-105">Syntax</span></span>

<span data-ttu-id="10243-106">*Expression* . CreateQueryDef (***имя***, ***склтекст***)</span><span class="sxs-lookup"><span data-stu-id="10243-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="10243-107">*Expression (выражение* ) Переменная, представляющая объект **Connection** .</span><span class="sxs-lookup"><span data-stu-id="10243-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="10243-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="10243-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10243-109">Имя</span><span class="sxs-lookup"><span data-stu-id="10243-109">Name</span></span></p></th>
<th><p><span data-ttu-id="10243-110">Обязательно/необязательно</span><span class="sxs-lookup"><span data-stu-id="10243-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="10243-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="10243-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="10243-112">Описание</span><span class="sxs-lookup"><span data-stu-id="10243-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10243-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="10243-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="10243-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="10243-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="10243-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="10243-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="10243-116"><strong>Variant</strong> (подтип<strong>String</strong> ), уникально названный новому <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="10243-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10243-117"><em>Склтекст</em></span><span class="sxs-lookup"><span data-stu-id="10243-117"><em>SQLText</em></span></span></p></td>
<td><p><span data-ttu-id="10243-118">Необязательный</span><span class="sxs-lookup"><span data-stu-id="10243-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="10243-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="10243-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="10243-120"><strong>Variant</strong> (подтип<strong>String</strong> ), который представляет собой инструкцию SQL, определяющую объект <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="10243-120">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>.</span></span> <span data-ttu-id="10243-121">Если опустить этот аргумент, можно определить объект <strong>QueryDef</strong> , задав его свойство <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> перед добавлением в коллекцию или после него.</span><span class="sxs-lookup"><span data-stu-id="10243-121">If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="10243-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10243-122">Return value</span></span>

<span data-ttu-id="10243-123">QueryDef</span><span class="sxs-lookup"><span data-stu-id="10243-123">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="10243-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="10243-124">Remarks</span></span>

<span data-ttu-id="10243-125">Если при создании объекта **QueryDef**в рабочей области Microsoft Access для имени указана любая строка, отличная от нулевой длины, полученный объект **QueryDef** автоматически добавляется в коллекцию **[QueryDef](querydefs-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="10243-125">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="10243-126">Если объект, указанный по имени, уже является членом коллекции **QueryDef** , возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="10243-126">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="10243-127">Вы можете создать временный объект **QueryDef** , используя строку нулевой длины для аргумента name при выполнении метода **CreateQueryDef** .</span><span class="sxs-lookup"><span data-stu-id="10243-127">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="10243-128">Это также можно сделать, задав для свойства **[Name](connection-name-property-dao.md)** созданного экземпляра **QueryDef** пустую строку ("").</span><span class="sxs-lookup"><span data-stu-id="10243-128">You can also accomplish this by setting the **[Name](connection-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> <span data-ttu-id="10243-129">Временные объекты **QueryDef** удобно использовать, если вы хотите многократно использовать динамические инструкции SQL без необходимости создавать новые постоянные объекты в коллекции **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="10243-129">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="10243-130">Невозможно добавить временный объект **QueryDef** в коллекцию, так как строка нулевой длины не является допустимым именем для постоянного объекта **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="10243-130">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="10243-131">Вы всегда можете задать свойства **Name** и **SQL** нового объекта **QueryDef** , а затем добавить объект **QueryDef** в коллекцию **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="10243-131">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="10243-132">Чтобы выполнить инструкцию SQL в объекте **QueryDef** , используйте метод **[EXECUTE](connection-execute-method-dao.md)** или **[OpenRecordset](connection-openrecordset-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="10243-132">To run the SQL statement in a **QueryDef** object, use the **[Execute](connection-execute-method-dao.md)** or **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="10243-133">Использование объекта **QueryDef** является предпочтительным способом выполнения запросов к серверу SQL с помощью баз данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="10243-133">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="10243-134">Чтобы удалить объект **QueryDef** из коллекции **QueryDef** в базе данных ядра СУБД Microsoft Access, используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="10243-134">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

