---
title: Свойство index. Required (DAO)
TOCTitle: Required Property
ms:assetid: ec8fafc4-8155-c48e-b3c8-2d9be425175a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836310(v=office.15)
ms:contentKeyID: 48548518
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052963
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2660a4cb422d91cf46b98a8d3870d2ab2db73fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291701"
---
# <a name="indexrequired-property-dao"></a><span data-ttu-id="f2be1-102">Свойство index. Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="f2be1-102">Index.Required property (DAO)</span></span>

<span data-ttu-id="f2be1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2be1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f2be1-104">Задает или возвращает значение, которое указывает, требуется ли для объекта **[field](field-object-dao.md)** значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="f2be1-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2be1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2be1-105">Syntax</span></span>

<span data-ttu-id="f2be1-106">*Expression* . Обязательно</span><span class="sxs-lookup"><span data-stu-id="f2be1-106">*expression* .Required</span></span>

<span data-ttu-id="f2be1-107">*Expression (выражение* ) Переменная, представляющая объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="f2be1-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2be1-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="f2be1-108">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="f2be1-109">Если вы можете задать это свойство для объекта **индекса** или объекта **field** , задайте для объекта **field** .</span><span class="sxs-lookup"><span data-stu-id="f2be1-109">When you can set this property for either an **Index** object or a **Field** object, set it for the **Field** object.</span></span> <span data-ttu-id="f2be1-110">Срок действия параметра свойства для объекта **field** проверяется до объекта **index** .</span><span class="sxs-lookup"><span data-stu-id="f2be1-110">The validity of the property setting for a **Field** object is checked before that of an **Index** object.</span></span>

<span data-ttu-id="f2be1-111">Доступность обязательного свойства \*\*\*\* зависит от объекта, содержащего коллекцию Fields, [](fields-collection-dao.md) как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f2be1-111">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2be1-112">Если коллекция Fields принадлежит к элементу</span><span class="sxs-lookup"><span data-stu-id="f2be1-112">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="f2be1-113">Затем необходимо</span><span class="sxs-lookup"><span data-stu-id="f2be1-113">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2be1-114">Объект <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="f2be1-114"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f2be1-115">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f2be1-115">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2be1-116">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="f2be1-116"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f2be1-117">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2be1-117">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2be1-118">Объект <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="f2be1-118"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f2be1-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2be1-119">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2be1-120">Объект <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="f2be1-120"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f2be1-121">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f2be1-121">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2be1-122">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="f2be1-122"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f2be1-123">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f2be1-123">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

