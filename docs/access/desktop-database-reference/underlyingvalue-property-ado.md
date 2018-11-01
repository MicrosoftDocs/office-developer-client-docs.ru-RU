---
title: Свойство UnderlyingValue (ADO)
TOCTitle: UnderlyingValue property (ADO)
ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15)
ms:contentKeyID: 48548782
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d91dccb88ff39ad344ffa0e59e7ccdaaa9f1565
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867785"
---
# <a name="underlyingvalue-property-ado"></a><span data-ttu-id="8f437-102">Свойство UnderlyingValue (ADO)</span><span class="sxs-lookup"><span data-stu-id="8f437-102">UnderlyingValue property (ADO)</span></span>


<span data-ttu-id="8f437-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f437-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="8f437-104">Указывает объект [поля](field-object-ado.md) текущим значением в базе данных.</span><span class="sxs-lookup"><span data-stu-id="8f437-104">Indicates a [Field](field-object-ado.md) object's current value in the database.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f437-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f437-105">Return value</span></span>

<span data-ttu-id="8f437-106">Возвращает значение **типа Variant** , которое указывает значение **поля**.</span><span class="sxs-lookup"><span data-stu-id="8f437-106">Returns a **Variant** value that indicates the value of the **Field**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f437-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="8f437-107">Remarks</span></span>

<span data-ttu-id="8f437-108">Свойство **UnderlyingValue** возвращает текущее значение поля из базы данных.</span><span class="sxs-lookup"><span data-stu-id="8f437-108">Use the **UnderlyingValue** property to return the current field value from the database.</span></span> <span data-ttu-id="8f437-109">Значение поля в свойстве **UnderlyingValue** — это значение, которое будет отображаться транзакции и может быть вызвана последнее обновление с другой транзакции.</span><span class="sxs-lookup"><span data-stu-id="8f437-109">The field value in the **UnderlyingValue** property is the value that is visible to your transaction and may be the result of a recent update by another transaction.</span></span> <span data-ttu-id="8f437-110">Могут отличаться от свойств [OriginalValue](originalvalue-property-ado.md) , который отражает значение, которое было изначально возвращаемых [записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8f437-110">This may differ from the [OriginalValue](originalvalue-property-ado.md) property, which reflects the value that was originally returned to the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="8f437-111">Это похоже на использование метода [выполнить повторную синхронизацию](resync-method-ado.md) , но это свойство **UnderlyingValue** возвращает только значение определенного поля из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="8f437-111">This is similar to using the [Resync](resync-method-ado.md) method, but the **UnderlyingValue** property returns only the value for a specific field from the current record.</span></span> <span data-ttu-id="8f437-112">Это то же значение, которое использует метод [выполнить повторную синхронизацию](resync-method-ado.md) для замены свойства [Value](value-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="8f437-112">This is the same value that the [Resync](resync-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="8f437-113">При использовании этого свойства с помощью свойства **OriginalValue** можно разрешения конфликтов с помощью пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="8f437-113">When you use this property with the **OriginalValue** property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="8f437-114">Запись</span><span class="sxs-lookup"><span data-stu-id="8f437-114">Record</span></span>

<span data-ttu-id="8f437-115">Для [записи](record-object-ado.md) объектов это свойство будет пустым для полей, добавлены, прежде чем будет вызван метод [Update](update-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="8f437-115">For [Record](record-object-ado.md) objects, this property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

