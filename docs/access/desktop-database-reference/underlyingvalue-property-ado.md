---
title: Свойство UnderlyingValue (ADO)
TOCTitle: UnderlyingValue property (ADO)
ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15)
ms:contentKeyID: 48548782
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6d1618a0cb310c1e564fe18289da6a2d35e91d0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314002"
---
# <a name="underlyingvalue-property-ado"></a><span data-ttu-id="627ea-102">Свойство UnderlyingValue (ADO)</span><span class="sxs-lookup"><span data-stu-id="627ea-102">UnderlyingValue property (ADO)</span></span>


<span data-ttu-id="627ea-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="627ea-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="627ea-104">Указывает текущее значение объекта [field](field-object-ado.md) в базе данных.</span><span class="sxs-lookup"><span data-stu-id="627ea-104">Indicates a [Field](field-object-ado.md) object's current value in the database.</span></span>

## <a name="return-value"></a><span data-ttu-id="627ea-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="627ea-105">Return value</span></span>

<span data-ttu-id="627ea-106">Возвращает значение **типа Variant** , которое указывает значение **поля**.</span><span class="sxs-lookup"><span data-stu-id="627ea-106">Returns a **Variant** value that indicates the value of the **Field**.</span></span>

## <a name="remarks"></a><span data-ttu-id="627ea-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="627ea-107">Remarks</span></span>

<span data-ttu-id="627ea-108">Используйте свойство **UnderlyingValue** , чтобы возвратить значение текущего поля из базы данных.</span><span class="sxs-lookup"><span data-stu-id="627ea-108">Use the **UnderlyingValue** property to return the current field value from the database.</span></span> <span data-ttu-id="627ea-109">Значение поля в свойстве **UnderlyingValue** является значением, видимым для транзакции, и может быть результатом последнего обновления другой транзакции.</span><span class="sxs-lookup"><span data-stu-id="627ea-109">The field value in the **UnderlyingValue** property is the value that is visible to your transaction and may be the result of a recent update by another transaction.</span></span> <span data-ttu-id="627ea-110">Это может отличаться от свойства [originalValue](originalvalue-property-ado.md) , которое отражает значение, которое изначально было возвращено в [набор записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="627ea-110">This may differ from the [OriginalValue](originalvalue-property-ado.md) property, which reflects the value that was originally returned to the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="627ea-111">Это аналогично использованию метода [Resync](resync-method-ado.md) , но свойство **UnderlyingValue** возвращает только значение определенного поля из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="627ea-111">This is similar to using the [Resync](resync-method-ado.md) method, but the **UnderlyingValue** property returns only the value for a specific field from the current record.</span></span> <span data-ttu-id="627ea-112">Это то же значение, которое метод [Resync](resync-method-ado.md) использует для замены свойства [value](value-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="627ea-112">This is the same value that the [Resync](resync-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="627ea-113">При использовании этого свойства со свойством **originalValue** можно устранить конфликты, возникающие при пакетном обновлении.</span><span class="sxs-lookup"><span data-stu-id="627ea-113">When you use this property with the **OriginalValue** property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="627ea-114">Record</span><span class="sxs-lookup"><span data-stu-id="627ea-114">Record</span></span>

<span data-ttu-id="627ea-115">Для объектов [Record](record-object-ado.md) это свойство будет пустым для полей, добавленных перед вызовом метода [Update](update-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="627ea-115">For [Record](record-object-ado.md) objects, this property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

