---
<span data-ttu-id="d7d6e-101"><<<<<<< Название HEAD: TOCTitle имя свойства (ADO): имя свойства (ADO) === title: имя свойства (ADO) TOCTitle: имя свойства (ADO)</span><span class="sxs-lookup"><span data-stu-id="d7d6e-101"><<<<<<< HEAD title: Name Property (ADO) TOCTitle: Name Property (ADO) ======= title: Name property (ADO) TOCTitle: Name property (ADO)</span></span>
>>>>>>> <span data-ttu-id="d7d6e-102">главные ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15) ms:contentKeyID: 48544683 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="d7d6e-102">master ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15) ms:contentKeyID: 48544683 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="d7d6e-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="d7d6e-103"><<<<<<< HEAD</span></span>
# <a name="name-property-ado"></a><span data-ttu-id="d7d6e-104">Name Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="d7d6e-104">Name Property (ADO)</span></span>
=======
# <a name="name-property-ado"></a><span data-ttu-id="d7d6e-105">Свойство Name (ADO)</span><span class="sxs-lookup"><span data-stu-id="d7d6e-105">Name property (ADO)</span></span>
>>>>>>> <span data-ttu-id="d7d6e-106">master</span><span class="sxs-lookup"><span data-stu-id="d7d6e-106">master</span></span>


<span data-ttu-id="d7d6e-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7d6e-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d7d6e-108">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="d7d6e-108">Indicates the name of an object.</span></span>

<span data-ttu-id="d7d6e-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="d7d6e-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="d7d6e-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d7d6e-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="d7d6e-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d7d6e-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="d7d6e-112">master</span><span class="sxs-lookup"><span data-stu-id="d7d6e-112">master</span></span>

<span data-ttu-id="d7d6e-113">Задает или возвращает **строковое** значение, указывающее имя объекта.</span><span class="sxs-lookup"><span data-stu-id="d7d6e-113">Sets or returns a **String** value that indicates the name of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7d6e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d7d6e-114">Remarks</span></span>

<span data-ttu-id="d7d6e-115">Используйте свойство **Name** назначение имени или получить имя объекта **команды**, **Свойства**, **поля**или **параметра** .</span><span class="sxs-lookup"><span data-stu-id="d7d6e-115">Use the **Name** property to assign a name to or retrieve the name of a **Command**, **Property**, **Field**, or **Parameter** object.</span></span>

<span data-ttu-id="d7d6e-116">Значение является чтение и запись в объект **команды** и только для чтения **свойство** объекта.</span><span class="sxs-lookup"><span data-stu-id="d7d6e-116">The value is read/write on a **Command** object and read-only on a **Property** object.</span></span>

<span data-ttu-id="d7d6e-117">Для объекта **поля** **имя** обычно доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d7d6e-117">For a **Field** object, **Name** is normally read-only.</span></span> <span data-ttu-id="d7d6e-118">Тем не менее для новых объектов **полей** , к коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md), **имя** — чтение и запись только после того, как указано [значение](value-property-ado.md) свойства для **поля** и имеет поставщика данных успешно добавлено новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="d7d6e-118">However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Name** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="d7d6e-119">Для **параметра** объектов еще не добавляются в коллекцию [параметров](parameters-collection-ado.md) свойство **Name** — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="d7d6e-119">For **Parameter** objects not yet appended to the [Parameters](parameters-collection-ado.md) collection, the **Name** property is read/write.</span></span> <span data-ttu-id="d7d6e-120">Для присоединенных объекты **параметров** и другие объекты свойства **Name** — только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d7d6e-120">For appended **Parameter** objects and all other objects, the **Name** property is read-only.</span></span> <span data-ttu-id="d7d6e-121">Имена не обязательно должно быть уникальным в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="d7d6e-121">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="d7d6e-122">Свойство **Name** объекта можно извлечь с помощью порядковый номер ссылки, после чего можно обратиться к объекту непосредственно по имени.</span><span class="sxs-lookup"><span data-stu-id="d7d6e-122">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="d7d6e-123">Например если rstMain.Properties(20). Имя дает возможность обновления, впоследствии можно ссылаться на это свойство как дает возможность обновления, впоследствии можно ссылаться на это свойство как rstMain.Properties("Updatability").</span><span class="sxs-lookup"><span data-stu-id="d7d6e-123">For example, if rstMain.Properties(20).Name yields Updatability , you can subsequently refer to this property as yields Updatability , you can subsequently refer to this property as rstMain.Properties("Updatability") .</span></span>

