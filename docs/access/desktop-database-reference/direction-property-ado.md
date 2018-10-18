---
<span data-ttu-id="a6dbc-101"><<<<<<< Название HEAD: TOCTitle свойство направление (ADO): свойство направление (ADO) === название: свойства Direction (ADO) TOCTitle: свойства Direction (ADO)</span><span class="sxs-lookup"><span data-stu-id="a6dbc-101"><<<<<<< HEAD title: Direction Property (ADO) TOCTitle: Direction Property (ADO) ======= title: Direction property (ADO) TOCTitle: Direction property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a6dbc-102">главные ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15) ms:contentKeyID: 48544823 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="a6dbc-102">master ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15) ms:contentKeyID: 48544823 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="a6dbc-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="a6dbc-103"><<<<<<< HEAD</span></span>
# <a name="direction-property-ado"></a><span data-ttu-id="a6dbc-104">Direction Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="a6dbc-104">Direction Property (ADO)</span></span>
=======
# <a name="direction-property-ado"></a><span data-ttu-id="a6dbc-105">Свойство Direction (ADO)</span><span class="sxs-lookup"><span data-stu-id="a6dbc-105">Direction property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a6dbc-106">master</span><span class="sxs-lookup"><span data-stu-id="a6dbc-106">master</span></span>


<span data-ttu-id="a6dbc-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6dbc-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a6dbc-108">Указывает [параметр](parameter-object-ado.md) представляет входного параметра, выходного параметра, входного и выходного параметра, или если параметр имеет значение, возвращаемое хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="a6dbc-108">Indicates whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, an input and an output parameter, or if the parameter is the return value from a stored procedure.</span></span>

<span data-ttu-id="a6dbc-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="a6dbc-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="a6dbc-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a6dbc-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="a6dbc-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a6dbc-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="a6dbc-112">master</span><span class="sxs-lookup"><span data-stu-id="a6dbc-112">master</span></span>

<span data-ttu-id="a6dbc-113">Задает или возвращает значение [ParameterDirectionEnum](parameterdirectionenum.md) .</span><span class="sxs-lookup"><span data-stu-id="a6dbc-113">Sets or returns a [ParameterDirectionEnum](parameterdirectionenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6dbc-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a6dbc-114">Remarks</span></span>

<span data-ttu-id="a6dbc-115">Используйте свойство **направление** для указания передается как параметр или из процедуры.</span><span class="sxs-lookup"><span data-stu-id="a6dbc-115">Use the **Direction** property to specify how a parameter is passed to or from a procedure.</span></span> <span data-ttu-id="a6dbc-116">Является ли данное свойство **направление** чтения/записи; Это позволяет работать с поставщиками, которые не возвращают эти сведения или задать эти сведения при отсутствии ADO, чтобы сделать дополнительного обращения к поставщику для получения сведений о параметрах.</span><span class="sxs-lookup"><span data-stu-id="a6dbc-116">The **Direction** property is read/write; this allows you to work with providers that don't return this information or to set this information when you don't want ADO to make an extra call to the provider to retrieve parameter information.</span></span>

<span data-ttu-id="a6dbc-117">Не все поставщики можно определить направление параметры их хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="a6dbc-117">Not all providers can determine the direction of parameters in their stored procedures.</span></span> <span data-ttu-id="a6dbc-118">В таких случаях необходимо задать свойство **направление** до выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="a6dbc-118">In these cases, you must set the **Direction** property before you execute the query.</span></span>

