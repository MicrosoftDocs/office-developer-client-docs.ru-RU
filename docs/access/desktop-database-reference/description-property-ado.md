---
<span data-ttu-id="e69b9-101"><<<<<<< Название HEAD: TOCTitle свойство Description (ADO): Свойство Description (ADO) === название: Свойство Description (ADO) TOCTitle: Свойство Description (ADO)</span><span class="sxs-lookup"><span data-stu-id="e69b9-101"><<<<<<< HEAD title: Description Property (ADO) TOCTitle: Description Property (ADO) ======= title: Description property (ADO) TOCTitle: Description property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e69b9-102">главные ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15) ms:contentKeyID: 48544064 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="e69b9-102">master ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15) ms:contentKeyID: 48544064 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="e69b9-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="e69b9-103"><<<<<<< HEAD</span></span>
# <a name="description-property-ado"></a><span data-ttu-id="e69b9-104">Description Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="e69b9-104">Description Property (ADO)</span></span>
=======
# <a name="description-property-ado"></a><span data-ttu-id="e69b9-105">Свойство Description (ADO)</span><span class="sxs-lookup"><span data-stu-id="e69b9-105">Description property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e69b9-106">master</span><span class="sxs-lookup"><span data-stu-id="e69b9-106">master</span></span>


<span data-ttu-id="e69b9-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e69b9-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e69b9-108">Описывает объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e69b9-108">Describes an [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="e69b9-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="e69b9-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="e69b9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e69b9-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="e69b9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e69b9-111">Return value</span></span>
>>>>>>> <span data-ttu-id="e69b9-112">master</span><span class="sxs-lookup"><span data-stu-id="e69b9-112">master</span></span>

<span data-ttu-id="e69b9-113">Возвращает значение типа **String** , содержащее описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="e69b9-113">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e69b9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e69b9-114">Remarks</span></span>

<span data-ttu-id="e69b9-115">Используйте свойство **Description** для получения краткое описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="e69b9-115">Use the **Description** property to obtain a short description of the error.</span></span> <span data-ttu-id="e69b9-116">Отображение этого свойства для оповещения пользователя об ошибке, не могут и не хотите обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="e69b9-116">Display this property to alert the user to an error that you cannot or do not want to handle.</span></span> <span data-ttu-id="e69b9-117">Строка будет получен из ADO или поставщика.</span><span class="sxs-lookup"><span data-stu-id="e69b9-117">The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="e69b9-118">Поставщики отвечают за передачей текст определенное сообщение об ошибке в ADO.</span><span class="sxs-lookup"><span data-stu-id="e69b9-118">Providers are responsible for passing specific error text to ADO.</span></span> <span data-ttu-id="e69b9-119">Добавляет объект [Error](error-object-ado.md) ADO коллекцию **ошибок** для каждого поставщика получает сообщение об ошибке или предупреждение его.</span><span class="sxs-lookup"><span data-stu-id="e69b9-119">ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives.</span></span> <span data-ttu-id="e69b9-120">Перечисление коллекции **ошибки** для ошибки, которые передает поставщика трассировки.</span><span class="sxs-lookup"><span data-stu-id="e69b9-120">Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>

