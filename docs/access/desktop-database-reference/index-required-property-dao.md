---
title: Свойство Index.Required (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703134"
---
# <a name="indexrequired-property-dao"></a><span data-ttu-id="f4e67-102">Свойство Index.Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="f4e67-102">Index.Required property (DAO)</span></span>

<span data-ttu-id="f4e67-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4e67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f4e67-104">Задает или возвращает значение, которое указывает, требуется ли объект **[поля](field-object-dao.md)** ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f4e67-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4e67-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4e67-105">Syntax</span></span>

<span data-ttu-id="f4e67-106">*выражение* . Обязательно</span><span class="sxs-lookup"><span data-stu-id="f4e67-106">*expression* .Required</span></span>

<span data-ttu-id="f4e67-107">*выражение* Переменная, которая представляет объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="f4e67-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4e67-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="f4e67-108">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="f4e67-109">При установке этого свойства для объекта **индекса** или объекта **поля** задайте его для объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="f4e67-109">When you can set this property for either an **Index** object or a **Field** object, set it for the **Field** object.</span></span> <span data-ttu-id="f4e67-110">Перед, объект **индекса** проверять правильность настройки свойства для объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="f4e67-110">The validity of the property setting for a **Field** object is checked before that of an **Index** object.</span></span>

<span data-ttu-id="f4e67-111">Доступность свойства **необходимые** зависит от объекта, который содержит коллекцию [полей](fields-collection-dao.md) , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f4e67-111">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4e67-112">Если принадлежит коллекции полей</span><span class="sxs-lookup"><span data-stu-id="f4e67-112">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="f4e67-113">Затем необходимо — это</span><span class="sxs-lookup"><span data-stu-id="f4e67-113">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4e67-114">Объект <strong>индекса</strong></span><span class="sxs-lookup"><span data-stu-id="f4e67-114"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f4e67-115">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f4e67-115">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4e67-116">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="f4e67-116"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f4e67-117">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4e67-117">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4e67-118">Объект <strong>набора записей</strong></span><span class="sxs-lookup"><span data-stu-id="f4e67-118"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f4e67-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4e67-119">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4e67-120"><strong>Отношения</strong> объектов</span><span class="sxs-lookup"><span data-stu-id="f4e67-120"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f4e67-121">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f4e67-121">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4e67-122">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="f4e67-122"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f4e67-123">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f4e67-123">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

