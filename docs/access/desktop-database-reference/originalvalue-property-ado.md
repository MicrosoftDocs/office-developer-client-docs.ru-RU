---
title: Свойство OriginalValue (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0724320e1aaa1e7bfd3ceab8cf54afd5921c7425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288184"
---
# <a name="originalvalue-property-ado"></a><span data-ttu-id="fc292-102">Свойство OriginalValue (ADO)</span><span class="sxs-lookup"><span data-stu-id="fc292-102">OriginalValue property (ADO)</span></span>

<span data-ttu-id="fc292-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc292-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc292-104">Указывает значение поля, которое [существовало](field-object-ado.md) в записи до внесения каких-либо изменений.</span><span class="sxs-lookup"><span data-stu-id="fc292-104">Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc292-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc292-105">Return value</span></span>

<span data-ttu-id="fc292-106">Возвращает значение **Variant,** которое представляет значение поля перед любым изменением.</span><span class="sxs-lookup"><span data-stu-id="fc292-106">Returns a **Variant** value that represents the value of a field prior to any change.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc292-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="fc292-107">Remarks</span></span>

<span data-ttu-id="fc292-108">Используйте свойство **OriginalValue** для возврата исходного значения поля из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="fc292-108">Use the **OriginalValue** property to return the original field value for a field from the current record.</span></span>

<span data-ttu-id="fc292-109">В режиме немедленного обновления *(в* котором поставщик записывает изменения в исходный источник данных после вызова метода [Update)](update-method-ado.md) свойство **OriginalValue** возвращает значение поля, которое существовало до любых изменений (то есть с момента последнего вызова метода **Update).**</span><span class="sxs-lookup"><span data-stu-id="fc292-109">In *immediate update mode* (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call).</span></span> <span data-ttu-id="fc292-110">Это то же значение, которое метод [CancelUpdate](cancelupdate-method-ado.md) использует для замены [свойства Value.](value-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="fc292-110">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="fc292-111">В режиме пакетного обновления *(в* котором поставщик кэшировать несколько изменений и записывает их в исходный источник данных только при вызове метода [UpdateBatch)](updatebatch-method-ado.md) свойство **OriginalValue** возвращает значение поля, которое существовало до любых изменений (то есть с момента последнего вызова метода **UpdateBatch).**</span><span class="sxs-lookup"><span data-stu-id="fc292-111">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call).</span></span> <span data-ttu-id="fc292-112">Это то же значение, которое метод [CancelBatch](cancelbatch-method-ado.md) использует для замены **свойства Value.**</span><span class="sxs-lookup"><span data-stu-id="fc292-112">This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property.</span></span> <span data-ttu-id="fc292-113">При использовании этого свойства со [свойством UnderlyingValue](underlyingvalue-property-ado.md) можно устранить конфликты, возникающие в результате пакетных обновлений.</span><span class="sxs-lookup"><span data-stu-id="fc292-113">When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="fc292-114">Record</span><span class="sxs-lookup"><span data-stu-id="fc292-114">Record</span></span>

<span data-ttu-id="fc292-115">Для [объектов Record](record-object-ado.md) свойство **OriginalValue** будет пустым для полей, добавленных перед тем, как будет [вызвано обновление.](update-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="fc292-115">For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

