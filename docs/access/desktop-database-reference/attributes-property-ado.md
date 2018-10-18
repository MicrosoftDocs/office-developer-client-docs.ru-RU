---
<span data-ttu-id="8864e-101"><<<<<<< Название HEAD: TOCTitle свойство атрибуты (ADO): свойство атрибуты (ADO) === название: атрибуты свойства (ADO) TOCTitle: атрибуты свойства (ADO)</span><span class="sxs-lookup"><span data-stu-id="8864e-101"><<<<<<< HEAD title: Attributes Property (ADO) TOCTitle: Attributes Property (ADO) ======= title: Attributes property (ADO) TOCTitle: Attributes property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8864e-102">главные ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15) ms:contentKeyID: 48544716 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="8864e-102">master ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15) ms:contentKeyID: 48544716 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="8864e-103">ado210.chm1231117 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="8864e-103">ado210.chm1231117 f1_categories:</span></span>
- <span data-ttu-id="8864e-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="8864e-104">Office.Version=v15</span></span>
---

<span data-ttu-id="8864e-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="8864e-105"><<<<<<< HEAD</span></span>
# <a name="attributes-property-ado"></a><span data-ttu-id="8864e-106">Attributes Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="8864e-106">Attributes Property (ADO)</span></span>
=======
# <a name="attributes-property-ado"></a><span data-ttu-id="8864e-107">Свойство Attributes (ADO)</span><span class="sxs-lookup"><span data-stu-id="8864e-107">Attributes property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8864e-108">master</span><span class="sxs-lookup"><span data-stu-id="8864e-108">master</span></span>


<span data-ttu-id="8864e-109">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8864e-109">**Applies to**: Access 2013 | Office 2013</span></span>


## <a name="attributes-property"></a><span data-ttu-id="8864e-110">Свойство Attributes</span><span class="sxs-lookup"><span data-stu-id="8864e-110">Attributes Property</span></span>

<span data-ttu-id="8864e-111">Указывает один или несколько характеристик объекта.</span><span class="sxs-lookup"><span data-stu-id="8864e-111">Indicates one or more characteristics of an object.</span></span>

<span data-ttu-id="8864e-112"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="8864e-112"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="8864e-113">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8864e-113">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="8864e-114">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8864e-114">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="8864e-115">master</span><span class="sxs-lookup"><span data-stu-id="8864e-115">master</span></span>

<span data-ttu-id="8864e-116">Задает или возвращает значение типа **Long** .</span><span class="sxs-lookup"><span data-stu-id="8864e-116">Sets or returns a **Long** value.</span></span>

<span data-ttu-id="8864e-117">Объект [подключения](connection-object-ado.md) является ли данное свойство **атрибуты** чтения и записи и его значение может быть сумма одно или несколько значений [XactAttributeEnum](xactattributeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="8864e-117">For a [Connection](connection-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of one or more [XactAttributeEnum](xactattributeenum.md) values.</span></span> <span data-ttu-id="8864e-118">Значение по умолчанию равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="8864e-118">The default is zero (0).</span></span>

<span data-ttu-id="8864e-119">Свойство **Attributes** — чтение и запись объект [параметра](parameter-object-ado.md) и его значение может быть сумма [ParameterAttributesEnum](parameterattributesenum.md) любого одно или несколько значений.</span><span class="sxs-lookup"><span data-stu-id="8864e-119">For a [Parameter](parameter-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of any one or more [ParameterAttributesEnum](parameterattributesenum.md) values.</span></span> <span data-ttu-id="8864e-120">Значение по умолчанию — **adParamSigned**.</span><span class="sxs-lookup"><span data-stu-id="8864e-120">The default is **adParamSigned**.</span></span>

<span data-ttu-id="8864e-121">Для объекта [поля](field-object-ado.md) свойство **Attributes** может быть сумма одно или несколько значений [FieldAttributeEnum](fieldattributeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="8864e-121">For a [Field](field-object-ado.md) object, the **Attributes** property can be the sum of one or more [FieldAttributeEnum](fieldattributeenum.md) values.</span></span> <span data-ttu-id="8864e-122">Обычно только для чтения, однако для новых объектов **полей** , которые добавляются коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md), **атрибуты** чтения и записи только в том случае, если свойство [Value](value-property-ado.md) для **поля** не указан и новое **поле** успешно добавлена поставщиком данных путем вызова метода [Update](update-method-ado.md) коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="8864e-122">It is normally read-only, However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Attributes** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the new **Field** has been successfully added by the data provider by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="8864e-123">Для [Свойства](property-object-ado.md) объекта свойство **Attributes** доступен только для чтения и его значение может быть сумма [PropertyAttributesEnum](propertyattributesenum.md) любого одно или несколько значений.</span><span class="sxs-lookup"><span data-stu-id="8864e-123">For a [Property](property-object-ado.md) object, the **Attributes** property is read-only, and its value can be the sum of any one or more [PropertyAttributesEnum](propertyattributesenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="8864e-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="8864e-124">Remarks</span></span>

<span data-ttu-id="8864e-125">Используйте свойство **Attributes** задает или возвращает характеристик объекты **подключения** , объекты **параметров** , объекты [поля](field-object-ado.md) и [Свойства](property-object-ado.md) объектов.</span><span class="sxs-lookup"><span data-stu-id="8864e-125">Use the **Attributes** property to set or return characteristics of **Connection** objects, **Parameter** objects, [Field](field-object-ado.md) objects, or [Property](property-object-ado.md) objects.</span></span>

<span data-ttu-id="8864e-126">При указании нескольких атрибутов можно суммирования соответствующие константы.</span><span class="sxs-lookup"><span data-stu-id="8864e-126">When you set multiple attributes, you can sum the appropriate constants.</span></span> <span data-ttu-id="8864e-127">Если задать значение свойства для сумм, включая несовместимые константы, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="8864e-127">If you set the property value to a sum including incompatible constants, an error occurs.</span></span>

<span data-ttu-id="8864e-128">**Службы удаленных данных об использовании** Это свойство недоступно на объект **подключения** со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="8864e-128">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

