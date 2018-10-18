---
<span data-ttu-id="2a6d5-101"><<<<<<< Название HEAD: TOCTitle свойство положение (ADO): свойство положение (ADO) === заголовок: установите свойство (ADO) TOCTitle: установите свойство (ADO)</span><span class="sxs-lookup"><span data-stu-id="2a6d5-101"><<<<<<< HEAD title: Position Property (ADO) TOCTitle: Position Property (ADO) ======= title: Position property (ADO) TOCTitle: Position property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2a6d5-102">главные ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15) ms:contentKeyID: 48546709 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="2a6d5-102">master ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15) ms:contentKeyID: 48546709 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="2a6d5-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="2a6d5-103"><<<<<<< HEAD</span></span>
# <a name="position-property-ado"></a><span data-ttu-id="2a6d5-104">Position Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="2a6d5-104">Position Property (ADO)</span></span>
=======
# <a name="position-property-ado"></a><span data-ttu-id="2a6d5-105">Свойство положение (ADO)</span><span class="sxs-lookup"><span data-stu-id="2a6d5-105">Position property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2a6d5-106">master</span><span class="sxs-lookup"><span data-stu-id="2a6d5-106">master</span></span>


<span data-ttu-id="2a6d5-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a6d5-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2a6d5-108">Указывает текущую позицию в объект [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="2a6d5-108">Indicates the current position within a [Stream](stream-object-ado.md) object.</span></span>

<span data-ttu-id="2a6d5-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="2a6d5-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="2a6d5-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2a6d5-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="2a6d5-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2a6d5-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="2a6d5-112">master</span><span class="sxs-lookup"><span data-stu-id="2a6d5-112">master</span></span>

<span data-ttu-id="2a6d5-113">Задает или возвращает значение типа **Long** , который определяет, в число байтов текущей позиции от начала потока.</span><span class="sxs-lookup"><span data-stu-id="2a6d5-113">Sets or returns a **Long** value that specifies the offset, in number of bytes, of the current position from the beginning of the stream.</span></span> <span data-ttu-id="2a6d5-114">Значение по умолчанию равно 0, который представляет первого байта ответа в потоке.</span><span class="sxs-lookup"><span data-stu-id="2a6d5-114">The default is 0, which represents the first byte in the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a6d5-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="2a6d5-115">Remarks</span></span>

<span data-ttu-id="2a6d5-116">Можно перемещать текущей позиции в точку после завершения потока.</span><span class="sxs-lookup"><span data-stu-id="2a6d5-116">The current position can be moved to a point after the end of the stream.</span></span> <span data-ttu-id="2a6d5-117">Если указать текущую позицию за пределами потока будет соответствующим образом увеличить [размер](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) объекта **потока** .</span><span class="sxs-lookup"><span data-stu-id="2a6d5-117">If you specify the current position beyond the end of the stream, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** object will be increased accordingly.</span></span> <span data-ttu-id="2a6d5-118">Любой новый байт, добавлены таким способом будет иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="2a6d5-118">Any new bytes added in this way will be null.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2a6d5-119"><STRONG>Положение</STRONG> всегда меры в байтах.</span><span class="sxs-lookup"><span data-stu-id="2a6d5-119"><STRONG>Position</STRONG> always measures bytes.</span></span> <span data-ttu-id="2a6d5-120">Для потоков текста с использованием многобайтовой кодировке умножьте положение на размер знаков для определения количества знаков.</span><span class="sxs-lookup"><span data-stu-id="2a6d5-120">For text streams using multibyte character sets, multiply the position by the character size to determine the character number.</span></span> <span data-ttu-id="2a6d5-121">Например для набор двухбайтовых знаков первым символом является позиции 0, второй символ в позиции 2, третий символ в позиции 4 и т. д.</span><span class="sxs-lookup"><span data-stu-id="2a6d5-121">For example, for a two-byte character set, the first character is at position 0, the second character at position 2, the third character at position 4, and so on.</span></span></P>



<span data-ttu-id="2a6d5-122">Отрицательные значения не может использоваться для изменения текущего положения в **потоке**.</span><span class="sxs-lookup"><span data-stu-id="2a6d5-122">Negative values cannot be used to change the current position in a **Stream**.</span></span> <span data-ttu-id="2a6d5-123">Для **позиции**можно использовать только положительными числами.</span><span class="sxs-lookup"><span data-stu-id="2a6d5-123">Only positive numbers can be used for **Position**.</span></span>

<span data-ttu-id="2a6d5-124">Для объектов **поток** только для чтения ADO не возвращает ошибку, если **положение** присвоено значение больше, чем **размер** **потока**.</span><span class="sxs-lookup"><span data-stu-id="2a6d5-124">For read-only **Stream** objects, ADO will not return an error if **Position** is set to a value greater than the **Size** of the **Stream**.</span></span> <span data-ttu-id="2a6d5-125">Это не изменять размер **потока**, и не изменяет содержимое **потока** никаких уведомлений.</span><span class="sxs-lookup"><span data-stu-id="2a6d5-125">This does not change the size of the **Stream**, or alter the **Stream** contents in any way.</span></span> <span data-ttu-id="2a6d5-126">Тем не менее при этом следует избегать, так как это приводит значение не имеет смысла **положение** .</span><span class="sxs-lookup"><span data-stu-id="2a6d5-126">However, doing this should be avoided because it results in a meaningless **Position** value.</span></span>

