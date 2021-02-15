---
title: Свойство Field.ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6d9ec790-a9d2-84d7-ccba-57d738491e36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195540(v=office.15)
ms:contentKeyID: 48545494
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47bd400469bc17ac2b57bb249198f7609d7d0801
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292932"
---
# <a name="fieldvalidationtext-property-dao"></a><span data-ttu-id="0c307-102">Свойство Field.ValidationText (DAO)</span><span class="sxs-lookup"><span data-stu-id="0c307-102">Field.ValidationText property (DAO)</span></span>


<span data-ttu-id="0c307-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c307-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0c307-104">Задает или возвращает значение, определяющее текст сообщения, которое отображает ваше приложение, если значение объекта **Field** не удовлетворяют правилу проверки, задаваемому настройкой параметра **ValidationRule** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0c307-104">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="0c307-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="0c307-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c307-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c307-106">Syntax</span></span>

<span data-ttu-id="0c307-107">*выражение .* ValidationText</span><span class="sxs-lookup"><span data-stu-id="0c307-107">*expression* .ValidationText</span></span>

<span data-ttu-id="0c307-108">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="0c307-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c307-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="0c307-109">Remarks</span></span>

<span data-ttu-id="0c307-110">Значение параметра или возвращаемого значения — это **строка,** указывка текста, отображаемого, если пользователь пытается ввести недопустимое значение для поля.</span><span class="sxs-lookup"><span data-stu-id="0c307-110">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field.</span></span> <span data-ttu-id="0c307-111">Для объекта, который еще не добавлен в коллекцию, это свойство предназначено для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0c307-111">For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="0c307-112">Для объекта Field использование свойства **ValidationText** зависит от объекта, который содержит коллекцию **[Fields,](fields-collection-dao.md)** к которой применится объект **Field,** как показано в следующей таблице. </span><span class="sxs-lookup"><span data-stu-id="0c307-112">For a **Field** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0c307-113">Объект, к</span><span class="sxs-lookup"><span data-stu-id="0c307-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="0c307-114">Использование</span><span class="sxs-lookup"><span data-stu-id="0c307-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c307-115"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="0c307-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="0c307-116">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0c307-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c307-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="0c307-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="0c307-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c307-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c307-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="0c307-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="0c307-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c307-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c307-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="0c307-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="0c307-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0c307-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c307-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="0c307-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="0c307-124">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c307-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

