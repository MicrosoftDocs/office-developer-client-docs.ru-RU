---
<span data-ttu-id="6a1c0-101"><<<<<<< Название HEAD: TOCTitle значение свойства (ADO): значение свойства (ADO) === название: значение свойства (ADO) TOCTitle: значение свойства (ADO)</span><span class="sxs-lookup"><span data-stu-id="6a1c0-101"><<<<<<< HEAD title: Value Property (ADO) TOCTitle: Value Property (ADO) ======= title: Value property (ADO) TOCTitle: Value property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6a1c0-102">главные ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15) ms:contentKeyID: 48548958 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="6a1c0-102">master ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15) ms:contentKeyID: 48548958 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="6a1c0-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="6a1c0-103"><<<<<<< HEAD</span></span>
# <a name="value-property-ado"></a><span data-ttu-id="6a1c0-104">Value Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="6a1c0-104">Value Property (ADO)</span></span>
=======
# <a name="value-property-ado"></a><span data-ttu-id="6a1c0-105">Свойство Value (ADO)</span><span class="sxs-lookup"><span data-stu-id="6a1c0-105">Value property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6a1c0-106">master</span><span class="sxs-lookup"><span data-stu-id="6a1c0-106">master</span></span>


<span data-ttu-id="6a1c0-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a1c0-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6a1c0-108">Указывает значение, присваиваемое [поля](field-object-ado.md), [параметр](parameter-object-ado.md)или [Свойства](property-object-ado.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="6a1c0-108">Indicates the value assigned to a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

<span data-ttu-id="6a1c0-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="6a1c0-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="6a1c0-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6a1c0-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="6a1c0-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6a1c0-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="6a1c0-112">master</span><span class="sxs-lookup"><span data-stu-id="6a1c0-112">master</span></span>

<span data-ttu-id="6a1c0-113">Задает или возвращает значение **типа Variant** , которое указывает значение объекта.</span><span class="sxs-lookup"><span data-stu-id="6a1c0-113">Sets or returns a **Variant** value that indicates the value of the object.</span></span> <span data-ttu-id="6a1c0-114">Значение по умолчанию зависит от [типа](type-property-ado.md) свойства.</span><span class="sxs-lookup"><span data-stu-id="6a1c0-114">Default value depends on the [Type](type-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a1c0-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="6a1c0-115">Remarks</span></span>

<span data-ttu-id="6a1c0-116">Используйте свойство **Value** задает или возвращает данные из **поля** объектов, изменять или возвращаемые значения параметра с объектами **параметров** для или установить параметры свойств с помощью **Свойства** объектов.</span><span class="sxs-lookup"><span data-stu-id="6a1c0-116">Use the **Value** property to set or return data from **Field** objects, to set or return parameter values with **Parameter** objects, or to set or return property settings with **Property** objects.</span></span> <span data-ttu-id="6a1c0-117">Является ли **значение** свойства чтения и записи или только для чтения зависит от множество факторов, обратитесь к соответствующим разделам соответствующего объекта для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="6a1c0-117">Whether the **Value** property is read/write or read-only depends upon numerous factors — see the respective object topics for more information.</span></span>

<span data-ttu-id="6a1c0-118">ADO позволяет установку и возврат двоичные данные с помощью свойства **Value** .</span><span class="sxs-lookup"><span data-stu-id="6a1c0-118">ADO allows setting and returning long binary data with the **Value** property.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6a1c0-119">Для <STRONG>параметра</STRONG> объекты ADO считывает свойство <STRONG>Value</STRONG> только один раз от поставщика.</span><span class="sxs-lookup"><span data-stu-id="6a1c0-119">For <STRONG>Parameter</STRONG> objects, ADO reads the <STRONG>Value</STRONG> property only once from the provider.</span></span> <span data-ttu-id="6a1c0-120">Если команда содержит <STRONG>параметр</STRONG> , свойство <STRONG>Value</STRONG> является пустым и создание <A href="recordset-object-ado.md">набора записей</A> с помощью команды, убедитесь, что после закрытия <STRONG>набора записей</STRONG> перед загрузкой свойство <STRONG>Value</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="6a1c0-120">If a command contains a <STRONG>Parameter</STRONG> whose <STRONG>Value</STRONG> property is empty, and you create a <A href="recordset-object-ado.md">Recordset</A> from the command, ensure that you first close the <STRONG>Recordset</STRONG> before retrieving the <STRONG>Value</STRONG> property.</span></span> <span data-ttu-id="6a1c0-121">В противном случае для некоторых поставщиков свойство <STRONG>Value</STRONG> может быть пустым и не содержит правильное значение.</span><span class="sxs-lookup"><span data-stu-id="6a1c0-121">Otherwise, for some providers, the <STRONG>Value</STRONG> property may be empty, and won't contain the correct value.</span></span></P>



<span data-ttu-id="6a1c0-122">Для нового **поля** объектов, к коллекции [полей](fields-collection-ado.md) объекта [записи](record-object-ado.md) свойство **Value** необходимо установить перед можно указать любые другие свойства **поля** .</span><span class="sxs-lookup"><span data-stu-id="6a1c0-122">For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, the **Value** property must be set before any other **Field** properties can be specified.</span></span> <span data-ttu-id="6a1c0-123">Во-первых определенного значения для свойства **Value** должна быть назначена и вызове [Update](update-method-ado.md) в коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="6a1c0-123">First, a specific value for the **Value** property must have been assigned and [Update](update-method-ado.md) on the **Fields** collection called.</span></span> <span data-ttu-id="6a1c0-124">Затем осуществляется другие свойства, такие как [Тип](type-property-ado.md) или [атрибуты](attributes-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="6a1c0-124">Then, other properties such as [Type](type-property-ado.md) or [Attributes](attributes-property-ado.md) can be accessed.</span></span>

