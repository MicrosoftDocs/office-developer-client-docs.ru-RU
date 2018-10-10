---
title: Field-Related Error Information
TOCTitle: Field-Related Error Information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dfa35220e463cada69c94fe56a72732591683686
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480361"
---
# <a name="field-related-error-information"></a><span data-ttu-id="2c324-102">Field-Related Error Information</span><span class="sxs-lookup"><span data-stu-id="2c324-102">Field-Related Error Information</span></span>


<span data-ttu-id="2c324-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c324-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2c324-104">Если ошибка, непосредственно связан с полем — например, если отсутствуют данные или имеет неверный тип поля — можно получить дополнительные сведения о причине проблемы, проверив свойство **состояние** объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="2c324-104">If an error is directly related to a field — for example, if the data is missing or if it is the wrong type for the field — you can retrieve more information about the cause of the problem by examining the **Field** object's **Status** property.</span></span> <span data-ttu-id="2c324-105">Это свойство улучшена для предоставления конкретной информации о проблеме.</span><span class="sxs-lookup"><span data-stu-id="2c324-105">This property has been enhanced to provide specific information about the problem.</span></span> <span data-ttu-id="2c324-106">Таким образом например, при сбое вызова **UpdateBatch** причины проблемы можно определить путем проверки свойство **Status** **полей** в каждой записи задействованных базах.</span><span class="sxs-lookup"><span data-stu-id="2c324-106">So, for example, when a call to **UpdateBatch** fails, the cause of the problem can be determined by examining the **Status** property of the **Fields** in each of the effected records.</span></span> <span data-ttu-id="2c324-107">Это свойство будет содержать одно из значений в **FieldStatusEnum** константу.</span><span class="sxs-lookup"><span data-stu-id="2c324-107">The property will contain one of the values in the **FieldStatusEnum** constant.</span></span> <span data-ttu-id="2c324-108">В следующей таблице представлены эти значения, которые могут представлять интерес при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="2c324-108">The following table includes those values that are of particular interest when an error occurs.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2c324-109">Константа</span><span class="sxs-lookup"><span data-stu-id="2c324-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="2c324-110">Значение</span><span class="sxs-lookup"><span data-stu-id="2c324-110">Value</span></span></p></th>
<th><p><span data-ttu-id="2c324-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2c324-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c324-112"><strong>adFieldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="2c324-112"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="2c324-113">2</span><span class="sxs-lookup"><span data-stu-id="2c324-113">2</span></span></p></td>
<td><p><span data-ttu-id="2c324-114">Указывает поля извлекается или хранятся без потери данных.</span><span class="sxs-lookup"><span data-stu-id="2c324-114">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c324-115"><strong>adFieldDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="2c324-115"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="2c324-116">6</span><span class="sxs-lookup"><span data-stu-id="2c324-116">6</span></span></p></td>
<td><p><span data-ttu-id="2c324-117">Указывает, что данные, возвращаемые от поставщика переполнена тип данных поля.</span><span class="sxs-lookup"><span data-stu-id="2c324-117">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c324-118"><strong>adFieldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="2c324-118"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="2c324-119">13</span><span class="sxs-lookup"><span data-stu-id="2c324-119">13</span></span></p></td>
<td><p><span data-ttu-id="2c324-120">Указывает, что значение по умолчанию для поля было использовано при задании данных.</span><span class="sxs-lookup"><span data-stu-id="2c324-120">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c324-121"><strong>adFieldIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="2c324-121"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="2c324-122">15</span><span class="sxs-lookup"><span data-stu-id="2c324-122">15</span></span></p></td>
<td><p><span data-ttu-id="2c324-123">Указывает, что это поле была пропущена при значения параметра данных в источнике.</span><span class="sxs-lookup"><span data-stu-id="2c324-123">Indicates that this field was skipped when setting data values in the source.</span></span> <span data-ttu-id="2c324-124">Значение не было установлено поставщиком.</span><span class="sxs-lookup"><span data-stu-id="2c324-124">No value was set by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c324-125"><strong>adFieldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="2c324-125"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="2c324-126">10</span><span class="sxs-lookup"><span data-stu-id="2c324-126">10</span></span></p></td>
<td><p><span data-ttu-id="2c324-127">Указывает, что поле нельзя изменить, так как они вычисляемые или производные сущности.</span><span class="sxs-lookup"><span data-stu-id="2c324-127">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c324-128"><strong>adFieldIsNull</strong></span><span class="sxs-lookup"><span data-stu-id="2c324-128"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="2c324-129">3</span><span class="sxs-lookup"><span data-stu-id="2c324-129">3</span></span></p></td>
<td><p><span data-ttu-id="2c324-130">Указывает, что поставщик возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="2c324-130">Indicates that the provider returned a null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c324-131"><strong>adFieldOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="2c324-131"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="2c324-132">22</span><span class="sxs-lookup"><span data-stu-id="2c324-132">22</span></span></p></td>
<td><p><span data-ttu-id="2c324-133">Указывает, что поставщик не удается получить достаточно дискового пространства для выполнения перемещения или копирования операции.</span><span class="sxs-lookup"><span data-stu-id="2c324-133">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
</tbody>
</table>

