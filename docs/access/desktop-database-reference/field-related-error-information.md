---
title: Сведения об ошибках, связанных с полями
TOCTitle: Field-related error information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a0d0362b8f0ff9570a92a3c1c364061d1f9a584
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292974"
---
# <a name="field-related-error-information"></a><span data-ttu-id="00ab0-102">Сведения об ошибках, связанных с полями</span><span class="sxs-lookup"><span data-stu-id="00ab0-102">Field-related error information</span></span>


<span data-ttu-id="00ab0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="00ab0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="00ab0-104">Если ошибка напрямую связана с полем ( например, если данные отсутствуют или неправильный тип поля), можно получить дополнительные сведения о причине проблемы, изучив свойство **Status** объекта **Field.**</span><span class="sxs-lookup"><span data-stu-id="00ab0-104">If an error is directly related to a field — for example, if the data is missing or if it is the wrong type for the field — you can retrieve more information about the cause of the problem by examining the **Field** object's **Status** property.</span></span> <span data-ttu-id="00ab0-105">Это свойство было усовершенствовано для предоставления определенных сведений о проблеме.</span><span class="sxs-lookup"><span data-stu-id="00ab0-105">This property has been enhanced to provide specific information about the problem.</span></span> <span data-ttu-id="00ab0-106">Например, если вызов **UpdateBatch** не удается, причину проблемы можно определить, изучив свойство  **Status** полей в каждой из зарегистрированных записей.</span><span class="sxs-lookup"><span data-stu-id="00ab0-106">So, for example, when a call to **UpdateBatch** fails, the cause of the problem can be determined by examining the **Status** property of the **Fields** in each of the effected records.</span></span> <span data-ttu-id="00ab0-107">Свойство будет содержать одно из значений в константе **FieldStatusEnum.**</span><span class="sxs-lookup"><span data-stu-id="00ab0-107">The property will contain one of the values in the **FieldStatusEnum** constant.</span></span> <span data-ttu-id="00ab0-108">В следующей таблице содержатся значения, которые могут быть интересны при ошибке.</span><span class="sxs-lookup"><span data-stu-id="00ab0-108">The following table includes those values that are of particular interest when an error occurs.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="00ab0-109">Константа</span><span class="sxs-lookup"><span data-stu-id="00ab0-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="00ab0-110">Значение</span><span class="sxs-lookup"><span data-stu-id="00ab0-110">Value</span></span></p></th>
<th><p><span data-ttu-id="00ab0-111">Описание</span><span class="sxs-lookup"><span data-stu-id="00ab0-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00ab0-112"><strong>adFieldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="00ab0-112"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="00ab0-113">2 </span><span class="sxs-lookup"><span data-stu-id="00ab0-113">2</span></span></p></td>
<td><p><span data-ttu-id="00ab0-114">Указывает, что поле не может быть извлечено или сохранено без потери данных.</span><span class="sxs-lookup"><span data-stu-id="00ab0-114">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ab0-115"><strong>adFieldDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="00ab0-115"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="00ab0-116">6 </span><span class="sxs-lookup"><span data-stu-id="00ab0-116">6</span></span></p></td>
<td><p><span data-ttu-id="00ab0-117">Указывает, что данные, возвращенные поставщиком, переполнили тип данных поля.</span><span class="sxs-lookup"><span data-stu-id="00ab0-117">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00ab0-118"><strong>adFieldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="00ab0-118"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="00ab0-119">13 </span><span class="sxs-lookup"><span data-stu-id="00ab0-119">13</span></span></p></td>
<td><p><span data-ttu-id="00ab0-120">Указывает, что значение по умолчанию для поля использовалось при установке данных.</span><span class="sxs-lookup"><span data-stu-id="00ab0-120">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ab0-121"><strong>adFieldIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="00ab0-121"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="00ab0-122">15 </span><span class="sxs-lookup"><span data-stu-id="00ab0-122">15</span></span></p></td>
<td><p><span data-ttu-id="00ab0-123">Указывает, что это поле было пропущено при установке значений данных в источнике.</span><span class="sxs-lookup"><span data-stu-id="00ab0-123">Indicates that this field was skipped when setting data values in the source.</span></span> <span data-ttu-id="00ab0-124">Поставщик не установил значение.</span><span class="sxs-lookup"><span data-stu-id="00ab0-124">No value was set by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00ab0-125"><strong>adFieldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="00ab0-125"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="00ab0-126">10 </span><span class="sxs-lookup"><span data-stu-id="00ab0-126">10</span></span></p></td>
<td><p><span data-ttu-id="00ab0-127">Указывает, что поле не может быть изменено, так как является вычисляемой или производной сущностью.</span><span class="sxs-lookup"><span data-stu-id="00ab0-127">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ab0-128"><strong>adFieldIsNull</strong></span><span class="sxs-lookup"><span data-stu-id="00ab0-128"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="00ab0-129">3 </span><span class="sxs-lookup"><span data-stu-id="00ab0-129">3</span></span></p></td>
<td><p><span data-ttu-id="00ab0-130">Указывает, что поставщик вернул значение null.</span><span class="sxs-lookup"><span data-stu-id="00ab0-130">Indicates that the provider returned a null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00ab0-131"><strong>adFieldOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="00ab0-131"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="00ab0-132">22</span><span class="sxs-lookup"><span data-stu-id="00ab0-132">22</span></span></p></td>
<td><p><span data-ttu-id="00ab0-133">Указывает, что поставщику не удается получить достаточно места для выполнения операции перемещения или копирования.</span><span class="sxs-lookup"><span data-stu-id="00ab0-133">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
</tbody>
</table>

