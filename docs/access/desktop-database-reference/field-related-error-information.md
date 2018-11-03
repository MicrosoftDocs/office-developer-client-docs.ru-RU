---
title: Сведения об ошибках, связанных с полями
TOCTitle: Field-related error information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e853c45e4ee0de9a958ccc791bac3afcd305a23
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943565"
---
# <a name="field-related-error-information"></a><span data-ttu-id="fff94-102">Сведения об ошибках, связанных с полями</span><span class="sxs-lookup"><span data-stu-id="fff94-102">Field-related error information</span></span>


<span data-ttu-id="fff94-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fff94-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fff94-104">Если ошибка, непосредственно связан с полем — например, если отсутствуют данные или имеет неверный тип поля — можно получить дополнительные сведения о причине проблемы, проверив свойство **состояние** объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="fff94-104">If an error is directly related to a field — for example, if the data is missing or if it is the wrong type for the field — you can retrieve more information about the cause of the problem by examining the **Field** object's **Status** property.</span></span> <span data-ttu-id="fff94-105">Это свойство улучшена для предоставления конкретной информации о проблеме.</span><span class="sxs-lookup"><span data-stu-id="fff94-105">This property has been enhanced to provide specific information about the problem.</span></span> <span data-ttu-id="fff94-106">Таким образом например, при сбое вызова **UpdateBatch** причины проблемы можно определить путем проверки свойство **Status** **полей** в каждой записи задействованных базах.</span><span class="sxs-lookup"><span data-stu-id="fff94-106">So, for example, when a call to **UpdateBatch** fails, the cause of the problem can be determined by examining the **Status** property of the **Fields** in each of the effected records.</span></span> <span data-ttu-id="fff94-107">Это свойство будет содержать одно из значений в **FieldStatusEnum** константу.</span><span class="sxs-lookup"><span data-stu-id="fff94-107">The property will contain one of the values in the **FieldStatusEnum** constant.</span></span> <span data-ttu-id="fff94-108">В следующей таблице представлены эти значения, которые могут представлять интерес при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="fff94-108">The following table includes those values that are of particular interest when an error occurs.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fff94-109">Константа</span><span class="sxs-lookup"><span data-stu-id="fff94-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="fff94-110">Значение</span><span class="sxs-lookup"><span data-stu-id="fff94-110">Value</span></span></p></th>
<th><p><span data-ttu-id="fff94-111">Описание</span><span class="sxs-lookup"><span data-stu-id="fff94-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fff94-112"><strong>adFieldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="fff94-112"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="fff94-113">2</span><span class="sxs-lookup"><span data-stu-id="fff94-113">2</span></span></p></td>
<td><p><span data-ttu-id="fff94-114">Указывает поля извлекается или хранятся без потери данных.</span><span class="sxs-lookup"><span data-stu-id="fff94-114">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fff94-115"><strong>adFieldDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="fff94-115"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="fff94-116">6</span><span class="sxs-lookup"><span data-stu-id="fff94-116">6</span></span></p></td>
<td><p><span data-ttu-id="fff94-117">Указывает, что данные, возвращаемые от поставщика переполнена тип данных поля.</span><span class="sxs-lookup"><span data-stu-id="fff94-117">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fff94-118"><strong>adFieldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="fff94-118"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="fff94-119">13</span><span class="sxs-lookup"><span data-stu-id="fff94-119">13</span></span></p></td>
<td><p><span data-ttu-id="fff94-120">Указывает, что значение по умолчанию для поля было использовано при задании данных.</span><span class="sxs-lookup"><span data-stu-id="fff94-120">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fff94-121"><strong>adFieldIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="fff94-121"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="fff94-122">15</span><span class="sxs-lookup"><span data-stu-id="fff94-122">15</span></span></p></td>
<td><p><span data-ttu-id="fff94-123">Указывает, что это поле была пропущена при значения параметра данных в источнике.</span><span class="sxs-lookup"><span data-stu-id="fff94-123">Indicates that this field was skipped when setting data values in the source.</span></span> <span data-ttu-id="fff94-124">Значение не было установлено поставщиком.</span><span class="sxs-lookup"><span data-stu-id="fff94-124">No value was set by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fff94-125"><strong>adFieldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="fff94-125"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="fff94-126">10</span><span class="sxs-lookup"><span data-stu-id="fff94-126">10</span></span></p></td>
<td><p><span data-ttu-id="fff94-127">Указывает, что поле нельзя изменить, так как они вычисляемые или производные сущности.</span><span class="sxs-lookup"><span data-stu-id="fff94-127">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fff94-128"><strong>adFieldIsNull</strong></span><span class="sxs-lookup"><span data-stu-id="fff94-128"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="fff94-129">3</span><span class="sxs-lookup"><span data-stu-id="fff94-129">3</span></span></p></td>
<td><p><span data-ttu-id="fff94-130">Указывает, что поставщик возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="fff94-130">Indicates that the provider returned a null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fff94-131"><strong>adFieldOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="fff94-131"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="fff94-132">22</span><span class="sxs-lookup"><span data-stu-id="fff94-132">22</span></span></p></td>
<td><p><span data-ttu-id="fff94-133">Указывает, что поставщик не удается получить достаточно дискового пространства для выполнения перемещения или копирования операции.</span><span class="sxs-lookup"><span data-stu-id="fff94-133">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
</tbody>
</table>

