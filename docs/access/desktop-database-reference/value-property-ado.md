---
title: Свойство Value (ADO)
TOCTitle: Value property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a61803648a0efa5f226b222fb54ce96c8aadbfe
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999059"
---
# <a name="value-property-ado"></a><span data-ttu-id="1c98d-102">Свойство Value (ADO)</span><span class="sxs-lookup"><span data-stu-id="1c98d-102">Value property (ADO)</span></span>

<span data-ttu-id="1c98d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c98d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c98d-104">Указывает значение, присваиваемое [поля](field-object-ado.md), [параметр](parameter-object-ado.md)или [Свойства](property-object-ado.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="1c98d-104">Indicates the value assigned to a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1c98d-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="1c98d-105">Settings and return values</span></span>

<span data-ttu-id="1c98d-106">Задает или возвращает значение **типа Variant** , которое указывает значение объекта.</span><span class="sxs-lookup"><span data-stu-id="1c98d-106">Sets or returns a **Variant** value that indicates the value of the object.</span></span> <span data-ttu-id="1c98d-107">Значение по умолчанию зависит от [типа](type-property-ado.md) свойства.</span><span class="sxs-lookup"><span data-stu-id="1c98d-107">Default value depends on the [Type](type-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c98d-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="1c98d-108">Remarks</span></span>

<span data-ttu-id="1c98d-109">Используйте свойство **Value** задает или возвращает данные из **поля** объектов, изменять или возвращаемые значения параметра с объектами **параметров** для или установить параметры свойств с помощью **Свойства** объектов.</span><span class="sxs-lookup"><span data-stu-id="1c98d-109">Use the **Value** property to set or return data from **Field** objects, to set or return parameter values with **Parameter** objects, or to set or return property settings with **Property** objects.</span></span> <span data-ttu-id="1c98d-110">Является ли **значение** свойства чтения и записи или только для чтения зависит от множество факторов, обратитесь к соответствующим разделам соответствующего объекта для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="1c98d-110">Whether the **Value** property is read/write or read-only depends upon numerous factors — see the respective object topics for more information.</span></span>

<span data-ttu-id="1c98d-111">ADO позволяет установку и возврат двоичные данные с помощью свойства **Value** .</span><span class="sxs-lookup"><span data-stu-id="1c98d-111">ADO allows setting and returning long binary data with the **Value** property.</span></span>

> [!NOTE]
> <span data-ttu-id="1c98d-112">Для **параметра** объекты ADO считывает свойство **Value** только один раз от поставщика.</span><span class="sxs-lookup"><span data-stu-id="1c98d-112">For **Parameter** objects, ADO reads the **Value** property only once from the provider.</span></span> <span data-ttu-id="1c98d-113">Если команда содержит **параметр** , свойство **Value** является пустым и создание [набора записей](recordset-object-ado.md) с помощью команды, убедитесь, что после закрытия **набора записей** перед загрузкой свойство **Value** .</span><span class="sxs-lookup"><span data-stu-id="1c98d-113">If a command contains a **Parameter** whose **Value** property is empty, and you create a [Recordset](recordset-object-ado.md) from the command, ensure that you first close the **Recordset** before retrieving the **Value** property.</span></span> <span data-ttu-id="1c98d-114">В противном случае для некоторых поставщиков свойство **Value** может быть пустым и не содержит правильное значение.</span><span class="sxs-lookup"><span data-stu-id="1c98d-114">Otherwise, for some providers, the **Value** property may be empty, and won't contain the correct value.</span></span>

<span data-ttu-id="1c98d-115">Для нового **поля** объектов, к коллекции [полей](fields-collection-ado.md) объекта [записи](record-object-ado.md) свойство **Value** необходимо установить перед можно указать любые другие свойства **поля** .</span><span class="sxs-lookup"><span data-stu-id="1c98d-115">For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, the **Value** property must be set before any other **Field** properties can be specified.</span></span> <span data-ttu-id="1c98d-116">Во-первых определенного значения для свойства **Value** должна быть назначена и вызове [Update](update-method-ado.md) в коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="1c98d-116">First, a specific value for the **Value** property must have been assigned and [Update](update-method-ado.md) on the **Fields** collection called.</span></span> <span data-ttu-id="1c98d-117">Затем осуществляется другие свойства, такие как [Тип](type-property-ado.md) или [атрибуты](attributes-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1c98d-117">Then, other properties such as [Type](type-property-ado.md) or [Attributes](attributes-property-ado.md) can be accessed.</span></span>

