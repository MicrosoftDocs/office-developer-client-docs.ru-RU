---
title: Свойство field2. ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4d58cb6bd32bd46b0a6bcec40ff68cdc52eebc31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292624"
---
# <a name="field2validationtext-property-dao"></a><span data-ttu-id="8d311-102">Свойство field2. ValidationText (DAO)</span><span class="sxs-lookup"><span data-stu-id="8d311-102">Field2.ValidationText property (DAO)</span></span>


<span data-ttu-id="8d311-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d311-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d311-104">Задает или возвращает значение, задающее текст сообщения, которое отображается в приложении, если значение объекта **field2** не удовлетворяет правилу проверки, заданному значением свойства **ValidationRule** (только для рабочих областей Microsoft Access ).</span><span class="sxs-lookup"><span data-stu-id="8d311-104">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field2** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="8d311-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="8d311-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d311-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d311-106">Syntax</span></span>

<span data-ttu-id="8d311-107">*Expression* . ValidationText</span><span class="sxs-lookup"><span data-stu-id="8d311-107">*expression* .ValidationText</span></span>

<span data-ttu-id="8d311-108">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="8d311-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d311-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="8d311-109">Remarks</span></span>

<span data-ttu-id="8d311-110">Параметр или возвращаемое значение — это **строка** , указывающая текст, который отображается, если пользователь пытается ввести недопустимое значение для поля.</span><span class="sxs-lookup"><span data-stu-id="8d311-110">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field.</span></span> <span data-ttu-id="8d311-111">Для объекта, который еще не добавлен в коллекцию, это свойство предназначено для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8d311-111">For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="8d311-112">Для объекта **field2** использование свойства **ValidationText** зависит от объекта, содержащего коллекцию Fields, к которой **[](fields-collection-dao.md)** добавляется объект **field2** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8d311-112">For a **Field2** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field2** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d311-113">Объект, добавленный в</span><span class="sxs-lookup"><span data-stu-id="8d311-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="8d311-114">Использование</span><span class="sxs-lookup"><span data-stu-id="8d311-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d311-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="8d311-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="8d311-116">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8d311-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d311-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="8d311-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="8d311-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d311-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d311-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="8d311-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="8d311-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d311-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d311-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="8d311-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="8d311-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8d311-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d311-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="8d311-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="8d311-124">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8d311-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

