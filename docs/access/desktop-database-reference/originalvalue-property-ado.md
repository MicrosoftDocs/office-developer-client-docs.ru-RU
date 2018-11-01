---
title: Свойство OriginalValue (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 872e7c88e5ea4e79d6bff4aa590e72743feb3893
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884914"
---
# <a name="originalvalue-property-ado"></a><span data-ttu-id="312dc-102">Свойство OriginalValue (ADO)</span><span class="sxs-lookup"><span data-stu-id="312dc-102">OriginalValue property (ADO)</span></span>

<span data-ttu-id="312dc-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="312dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="312dc-104">Указывает значение [поля](field-object-ado.md) , которое существовало в записи до внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="312dc-104">Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made.</span></span>

## <a name="return-value"></a><span data-ttu-id="312dc-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="312dc-105">Return value</span></span>

<span data-ttu-id="312dc-106">Возвращает значение **типа Variant** , который представляет значение поля до изменения.</span><span class="sxs-lookup"><span data-stu-id="312dc-106">Returns a **Variant** value that represents the value of a field prior to any change.</span></span>

## <a name="remarks"></a><span data-ttu-id="312dc-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="312dc-107">Remarks</span></span>

<span data-ttu-id="312dc-108">Свойство **OriginalValue** возвращает исходное значение поля для поля из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="312dc-108">Use the **OriginalValue** property to return the original field value for a field from the current record.</span></span>

<span data-ttu-id="312dc-109">В *режиме немедленное обновление* (где поставщик записывает изменения к базовому источнику данных после вызова метода [обновления](update-method-ado.md) ) это свойство **OriginalValue** возвращает значение поля, существовавшего до внесения изменений (то есть, поскольку Последнее **обновление** вызова метода).</span><span class="sxs-lookup"><span data-stu-id="312dc-109">In *immediate update mode* (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call).</span></span> <span data-ttu-id="312dc-110">Это то же значение, метод [CancelUpdate](cancelupdate-method-ado.md) используется для замены свойства [Value](value-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="312dc-110">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="312dc-111">В *пакетном режиме обновления* (в котором поставщик кэширует несколько изменений и записывает их в источнике данных только при вызове метода [UpdateBatch](updatebatch-method-ado.md) ) это свойство **OriginalValue** возвращает значение поля, существовавшего до какие-либо изменяет (то есть, с момента последнего метода **UpdateBatch** звонков).</span><span class="sxs-lookup"><span data-stu-id="312dc-111">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call).</span></span> <span data-ttu-id="312dc-112">Это то же значение, метод [CancelBatch](cancelbatch-method-ado.md) используется для замены свойства **Value** .</span><span class="sxs-lookup"><span data-stu-id="312dc-112">This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property.</span></span> <span data-ttu-id="312dc-113">При использовании этого свойства с помощью свойства [UnderlyingValue](underlyingvalue-property-ado.md) можно разрешения конфликтов с помощью пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="312dc-113">When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="312dc-114">Запись</span><span class="sxs-lookup"><span data-stu-id="312dc-114">Record</span></span>

<span data-ttu-id="312dc-115">Для [записи](record-object-ado.md) объектов **OriginalValue** свойство будет пустым для полей, добавлены, прежде чем будет вызван метод [Update](update-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="312dc-115">For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

