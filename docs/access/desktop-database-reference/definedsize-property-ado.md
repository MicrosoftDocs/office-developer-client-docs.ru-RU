---
<span data-ttu-id="1d847-101"><<<<<<< Название HEAD: TOCTitle свойство DefinedSize (ADO): свойство DefinedSize (ADO) === название: свойство DefinedSize (ADO) TOCTitle: свойство DefinedSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="1d847-101"><<<<<<< HEAD title: DefinedSize Property (ADO) TOCTitle: DefinedSize Property (ADO) ======= title: DefinedSize property (ADO) TOCTitle: DefinedSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="1d847-102">главные ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15) ms:contentKeyID: 48546257 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="1d847-102">master ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15) ms:contentKeyID: 48546257 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="1d847-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="1d847-103"><<<<<<< HEAD</span></span>
# <a name="definedsize-property-ado"></a><span data-ttu-id="1d847-104">DefinedSize Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="1d847-104">DefinedSize Property (ADO)</span></span>
=======
# <a name="definedsize-property-ado"></a><span data-ttu-id="1d847-105">Свойство DefinedSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="1d847-105">DefinedSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="1d847-106">master</span><span class="sxs-lookup"><span data-stu-id="1d847-106">master</span></span>


<span data-ttu-id="1d847-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d847-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1d847-108">Указывает объем данных объекта [поля](field-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1d847-108">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

<span data-ttu-id="1d847-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="1d847-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="1d847-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d847-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="1d847-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d847-111">Return value</span></span>
>>>>>>> <span data-ttu-id="1d847-112">master</span><span class="sxs-lookup"><span data-stu-id="1d847-112">master</span></span>

<span data-ttu-id="1d847-113">Возвращает значение типа **Long** , отражает определенный размер поля в байтах.</span><span class="sxs-lookup"><span data-stu-id="1d847-113">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d847-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="1d847-114">Remarks</span></span>

<span data-ttu-id="1d847-115">Свойство **DefinedSize** используется для определения емкости данных объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="1d847-115">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="1d847-116">Свойства **DefinedSize** и [ActualSize](actualsize-property-ado.md) не совпадают.</span><span class="sxs-lookup"><span data-stu-id="1d847-116">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different.</span></span> <span data-ttu-id="1d847-117">Например рассмотрим объект **Field** с типом объявленные **adVarChar** и значение свойства **DefinedSize** 50, содержащий один символ.</span><span class="sxs-lookup"><span data-stu-id="1d847-117">For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character.</span></span> <span data-ttu-id="1d847-118">**ActualSize** свойство возвращает значение длины в байтах один символ.</span><span class="sxs-lookup"><span data-stu-id="1d847-118">The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

