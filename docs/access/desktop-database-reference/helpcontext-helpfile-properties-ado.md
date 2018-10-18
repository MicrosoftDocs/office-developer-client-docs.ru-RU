---
<span data-ttu-id="a83e8-101"><<<<<<< Название HEAD: HelpContext, TOCTitle свойства HelpFile (ADO): HelpContext ms:assetid свойства HelpFile (ADO): 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 09/18 / 2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="a83e8-101"><<<<<<< HEAD title: HelpContext, HelpFile Properties (ADO) TOCTitle: HelpContext, HelpFile Properties (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="a83e8-102">HelpContext, HelpFile Properties (ADO)</span><span class="sxs-lookup"><span data-stu-id="a83e8-102">HelpContext, HelpFile Properties (ADO)</span></span>

<span data-ttu-id="a83e8-103">=== Название: HelpContext свойства HelpFile (ADO) TOCTitle: HelpContext HelpFile свойства (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 10/17/2018 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="a83e8-103">======= title: HelpContext, HelpFile properties (ADO) TOCTitle: HelpContext, HelpFile properties (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="a83e8-104">HelpContext свойства HelpFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="a83e8-104">HelpContext, HelpFile properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="a83e8-105">master</span><span class="sxs-lookup"><span data-stu-id="a83e8-105">master</span></span>

<span data-ttu-id="a83e8-106">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a83e8-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a83e8-107">Указывает файл справки и раздел, связанный с объектом [Ошибка](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a83e8-107">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="a83e8-108"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="a83e8-108"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="a83e8-109">Return Values</span><span class="sxs-lookup"><span data-stu-id="a83e8-109">Return Values</span></span>

  - <span data-ttu-id="a83e8-110">**HelpContextID** — возвращает идентификатор контекста, как **длинное целое** значение, для раздела в файле справки.</span><span class="sxs-lookup"><span data-stu-id="a83e8-110">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

  - <span data-ttu-id="a83e8-111">**Файл справки** — возвращает **строковое** значение, которое оценивается как полностью разрешенный путь к файлу справки.</span><span class="sxs-lookup"><span data-stu-id="a83e8-111">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="a83e8-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a83e8-112">Return values</span></span>

- <span data-ttu-id="a83e8-113">**HelpContextID** — возвращает идентификатор контекста, как **длинное целое** значение, для раздела в файле справки.</span><span class="sxs-lookup"><span data-stu-id="a83e8-113">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="a83e8-114">**Файл справки** — возвращает **строковое** значение, которое оценивается как полностью разрешенный путь к файлу справки.</span><span class="sxs-lookup"><span data-stu-id="a83e8-114">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>
>>>>>>> <span data-ttu-id="a83e8-115">master</span><span class="sxs-lookup"><span data-stu-id="a83e8-115">master</span></span>

## <a name="remarks"></a><span data-ttu-id="a83e8-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="a83e8-116">Remarks</span></span>

<span data-ttu-id="a83e8-117">Если в свойство **HelpFile** указан файл справки, свойство **HelpContext** используется для отображения раздела справки, он определяет автоматически.</span><span class="sxs-lookup"><span data-stu-id="a83e8-117">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies.</span></span> <span data-ttu-id="a83e8-118">Если нет ни один соответствующий раздел справки, свойство **HelpContext** возвращает нуль и свойство **HelpFile** возвращает строку нулевой длины (»»).</span><span class="sxs-lookup"><span data-stu-id="a83e8-118">If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>

