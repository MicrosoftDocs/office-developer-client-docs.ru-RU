---
title: Объект Property (ADO)
TOCTitle: Property Object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2fe6ac64417c5758d25872a7b67be7cb9f12ac6d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874511"
---
# <a name="property-object-ado"></a><span data-ttu-id="ec39b-102">Объект Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="ec39b-102">Property Object (ADO)</span></span>


<span data-ttu-id="ec39b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec39b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec39b-104">Представляет характеристику динамического объекта ADO, определяемый поставщиком.</span><span class="sxs-lookup"><span data-stu-id="ec39b-104">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec39b-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="ec39b-105">Remarks</span></span>

<span data-ttu-id="ec39b-106">Объекты ADO имеют два типа свойств: встроенные и динамические.</span><span class="sxs-lookup"><span data-stu-id="ec39b-106">ADO objects have two types of properties: built-in and dynamic.</span></span>

<span data-ttu-id="ec39b-107">Встроенные свойства — это свойства, реализованные в ADO и сразу же доступны для каждого нового объекта, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="ec39b-107">Built-in properties are those properties implemented in ADO and immediately available to any new object, using the syntax.</span></span> <span data-ttu-id="ec39b-108">Они не отображаются как **свойство** объектов в коллекции [свойств](properties-collection-ado.md) объекта, несмотря на то, что их значения можно изменить, не могут изменять их свойства.</span><span class="sxs-lookup"><span data-stu-id="ec39b-108">They do not appear as **Property** objects in an object's [Properties](properties-collection-ado.md) collection, so although you can change their values, you cannot modify their characteristics.</span></span>

<span data-ttu-id="ec39b-109">Динамические свойства определяются базового поставщика данных и отображаются в коллекцию **свойств** подходящий объект ADO.</span><span class="sxs-lookup"><span data-stu-id="ec39b-109">Dynamic properties are defined by the underlying data provider, and appear in the **Properties** collection for the appropriate ADO object.</span></span> <span data-ttu-id="ec39b-110">Например свойство поставщика может указывать, поддерживает ли объект [набора записей](recordset-object-ado.md) транзакций или обновление.</span><span class="sxs-lookup"><span data-stu-id="ec39b-110">For example, a property specific to the provider may indicate if a [Recordset](recordset-object-ado.md) object supports transactions or updating.</span></span> <span data-ttu-id="ec39b-111">Эти дополнительные свойства отображаются как **свойство** объектов в коллекции **свойств** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ec39b-111">These additional properties will appear as **Property** objects in that **Recordset** object's **Properties** collection.</span></span> <span data-ttu-id="ec39b-112">Динамические свойства можно ссылаться только с помощью коллекции, используя MyObject.Properties(0) или или синтаксис MyObject.Properties("Name").</span><span class="sxs-lookup"><span data-stu-id="ec39b-112">Dynamic properties can be referenced only through the collection, using the MyObject.Properties(0) or or MyObject.Properties("Name") syntax.</span></span>

<span data-ttu-id="ec39b-113">Не удается удалить любой тип свойства.</span><span class="sxs-lookup"><span data-stu-id="ec39b-113">You cannot delete either kind of property.</span></span>

<span data-ttu-id="ec39b-114">Объект динамического **Свойства** имеет четыре встроенных свойства свои собственные.</span><span class="sxs-lookup"><span data-stu-id="ec39b-114">A dynamic **Property** object has four built-in properties of its own:</span></span>

  - <span data-ttu-id="ec39b-115">Свойство [Name](name-property-ado.md) — это строка, которая определяет свойство.</span><span class="sxs-lookup"><span data-stu-id="ec39b-115">The [Name](name-property-ado.md) property is a string that identifies the property.</span></span>

  - <span data-ttu-id="ec39b-116">Свойство [Type](type-property-ado.md) — целое число, определяющее тип данных свойства.</span><span class="sxs-lookup"><span data-stu-id="ec39b-116">The [Type](type-property-ado.md) property is an integer that specifies the property data type.</span></span>

  - <span data-ttu-id="ec39b-117">Свойство [Value](value-property-ado.md) имеет тип variant, содержащее значение свойства.</span><span class="sxs-lookup"><span data-stu-id="ec39b-117">The [Value](value-property-ado.md) property is a variant that contains the property setting.</span></span> <span data-ttu-id="ec39b-118">**Значение** является свойством по умолчанию для **Свойства** объекта.</span><span class="sxs-lookup"><span data-stu-id="ec39b-118">**Value** is the default property for a **Property** object.</span></span>

  - <span data-ttu-id="ec39b-119">Свойство [Attributes](attributes-property-ado.md) — это значение типа long, указывающее характеристики свойства поставщика.</span><span class="sxs-lookup"><span data-stu-id="ec39b-119">The [Attributes](attributes-property-ado.md) property is a long value that indicates characteristics of the property specific to the provider.</span></span>

