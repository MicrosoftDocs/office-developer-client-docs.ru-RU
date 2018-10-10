---
title: UnderlyingValue Property (ADO)
TOCTitle: UnderlyingValue Property (ADO)
ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15)
ms:contentKeyID: 48548782
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10140d0cc4105ed46ddaaf48e4c827f364adc90c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481916"
---
# <a name="underlyingvalue-property-ado"></a><span data-ttu-id="24597-102">UnderlyingValue Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="24597-102">UnderlyingValue Property (ADO)</span></span>


<span data-ttu-id="24597-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="24597-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="24597-104">Указывает объект [поля](field-object-ado.md) текущим значением в базе данных.</span><span class="sxs-lookup"><span data-stu-id="24597-104">Indicates a [Field](field-object-ado.md) object's current value in the database.</span></span>

## <a name="return-value"></a><span data-ttu-id="24597-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24597-105">Return Value</span></span>

<span data-ttu-id="24597-106">Возвращает значение **типа Variant** , которое указывает значение **поля**.</span><span class="sxs-lookup"><span data-stu-id="24597-106">Returns a **Variant** value that indicates the value of the **Field**.</span></span>

## <a name="remarks"></a><span data-ttu-id="24597-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="24597-107">Remarks</span></span>

<span data-ttu-id="24597-108">Свойство **UnderlyingValue** возвращает текущее значение поля из базы данных.</span><span class="sxs-lookup"><span data-stu-id="24597-108">Use the **UnderlyingValue** property to return the current field value from the database.</span></span> <span data-ttu-id="24597-109">Значение поля в свойстве **UnderlyingValue** — это значение, которое будет отображаться транзакции и может быть вызвана последнее обновление с другой транзакции.</span><span class="sxs-lookup"><span data-stu-id="24597-109">The field value in the **UnderlyingValue** property is the value that is visible to your transaction and may be the result of a recent update by another transaction.</span></span> <span data-ttu-id="24597-110">Могут отличаться от свойств [OriginalValue](originalvalue-property-ado.md) , который отражает значение, которое было изначально возвращаемых [записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="24597-110">This may differ from the [OriginalValue](originalvalue-property-ado.md) property, which reflects the value that was originally returned to the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="24597-111">Это похоже на использование метода [выполнить повторную синхронизацию](resync-method-ado.md) , но это свойство **UnderlyingValue** возвращает только значение определенного поля из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="24597-111">This is similar to using the [Resync](resync-method-ado.md) method, but the **UnderlyingValue** property returns only the value for a specific field from the current record.</span></span> <span data-ttu-id="24597-112">Это то же значение, которое использует метод [выполнить повторную синхронизацию](resync-method-ado.md) для замены свойства [Value](value-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="24597-112">This is the same value that the [Resync](resync-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="24597-113">При использовании этого свойства с помощью свойства **OriginalValue** можно разрешения конфликтов с помощью пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="24597-113">When you use this property with the **OriginalValue** property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="24597-114">Запись</span><span class="sxs-lookup"><span data-stu-id="24597-114">Record</span></span>

<span data-ttu-id="24597-115">Для [записи](record-object-ado.md) объектов это свойство будет пустым для полей, добавлены, прежде чем будет вызван метод [Update](update-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="24597-115">For [Record](record-object-ado.md) objects, this property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

