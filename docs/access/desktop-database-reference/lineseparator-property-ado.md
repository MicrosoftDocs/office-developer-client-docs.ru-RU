---
<span data-ttu-id="0df29-101"><<<<<<< Название HEAD: TOCTitle свойство LineSeparator (ADO): свойство LineSeparator (ADO) === название: свойство LineSeparator (ADO) TOCTitle: свойство LineSeparator (ADO)</span><span class="sxs-lookup"><span data-stu-id="0df29-101"><<<<<<< HEAD title: LineSeparator Property (ADO) TOCTitle: LineSeparator Property (ADO) ======= title: LineSeparator property (ADO) TOCTitle: LineSeparator property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0df29-102">главные ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15) ms:contentKeyID: 48546676 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="0df29-102">master ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15) ms:contentKeyID: 48546676 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="0df29-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="0df29-103"><<<<<<< HEAD</span></span>
# <a name="lineseparator-property-ado"></a><span data-ttu-id="0df29-104">LineSeparator Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="0df29-104">LineSeparator Property (ADO)</span></span>
=======
# <a name="lineseparator-property-ado"></a><span data-ttu-id="0df29-105">Свойство LineSeparator (ADO)</span><span class="sxs-lookup"><span data-stu-id="0df29-105">LineSeparator property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0df29-106">master</span><span class="sxs-lookup"><span data-stu-id="0df29-106">master</span></span>


<span data-ttu-id="0df29-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0df29-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0df29-108">Указывает двоичных символов для использования в качестве разделителя строки в объектах [потока](stream-object-ado.md) текста.</span><span class="sxs-lookup"><span data-stu-id="0df29-108">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

<span data-ttu-id="0df29-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="0df29-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="0df29-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="0df29-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="0df29-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="0df29-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="0df29-112">master</span><span class="sxs-lookup"><span data-stu-id="0df29-112">master</span></span>

<span data-ttu-id="0df29-113">Задает или возвращает [LineSeparatorsEnum](lineseparatorsenum.md) значение, указывающее знак разделителя строки, используемые в **поток**.</span><span class="sxs-lookup"><span data-stu-id="0df29-113">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**.</span></span> <span data-ttu-id="0df29-114">Значение по умолчанию — **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="0df29-114">The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0df29-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="0df29-115">Remarks</span></span>

<span data-ttu-id="0df29-116">**LineSeparator** используется для интерпретации строки при чтении содержимое текста **потока**.</span><span class="sxs-lookup"><span data-stu-id="0df29-116">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**.</span></span> <span data-ttu-id="0df29-117">С помощью метода [SkipLine](skipline-method-ado.md) можно пропустить строки.</span><span class="sxs-lookup"><span data-stu-id="0df29-117">Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="0df29-118">**LineSeparator** используется только с объектами **потока** текста ([Тип](type-property-ado-stream.md) — **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="0df29-118">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="0df29-119">Это свойство игнорируется, если **Тип** — **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="0df29-119">This property is ignored if **Type** is **adTypeBinary**.</span></span>

