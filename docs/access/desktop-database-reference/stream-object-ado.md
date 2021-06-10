---
title: Объект Stream (ADO)
TOCTitle: Stream object (ADO)
ms:assetid: d49b1514-e0b4-0aca-d5c2-8266f3f4fe65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250065(v=office.15)
ms:contentKeyID: 48547945
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1f6d7e8f64f6b14ea699006fc0461cdf0ded2a06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308486"
---
# <a name="stream-object-ado"></a><span data-ttu-id="82429-102">Объект Stream (ADO)</span><span class="sxs-lookup"><span data-stu-id="82429-102">Stream object (ADO)</span></span>


<span data-ttu-id="82429-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="82429-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82429-104">Представляет поток двоичных данных или текста.</span><span class="sxs-lookup"><span data-stu-id="82429-104">Represents a stream of binary data or text.</span></span>

## <a name="remarks"></a><span data-ttu-id="82429-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="82429-105">Remarks</span></span>

<span data-ttu-id="82429-106">В иерархиях, структурированных на дереве, таких как [](record-object-ado.md) файловая система или система электронной почты, запись может иметь двоичный поток битов, связанных с ним по умолчанию, который содержит содержимое файла или электронной почты.</span><span class="sxs-lookup"><span data-stu-id="82429-106">In tree-structured hierarchies such as a file system or an email system, a [Record](record-object-ado.md) may have a default binary stream of bits associated with it that contains the contents of the file or the email.</span></span> <span data-ttu-id="82429-107">Объект **Stream** можно использовать для управления полями или записями, содержащими эти потоки данных.</span><span class="sxs-lookup"><span data-stu-id="82429-107">A **Stream** object can be used to manipulate fields or records containing these streams of data.</span></span> <span data-ttu-id="82429-108">Объект **Stream** можно получить таким образом:</span><span class="sxs-lookup"><span data-stu-id="82429-108">A **Stream** object can be obtained in these ways:</span></span>

  - <span data-ttu-id="82429-109">От URL-адреса, указыващего на объект (как правило, файл), содержащий двоичные или текстовые данные.</span><span class="sxs-lookup"><span data-stu-id="82429-109">From a URL pointing to an object (typically a file) containing binary or text data.</span></span> <span data-ttu-id="82429-110">Этот объект может быть простым документом, **объектом Record,** представляющим структурированный документ, или папкой.</span><span class="sxs-lookup"><span data-stu-id="82429-110">This object can be a simple document, a **Record** object representing a structured document, or a folder.</span></span>

  - <span data-ttu-id="82429-111">Открыв объект Stream **по** умолчанию, связанный с **объектом Record.**</span><span class="sxs-lookup"><span data-stu-id="82429-111">By opening the default **Stream** object associated with a **Record** object.</span></span> <span data-ttu-id="82429-112">Вы можете получить поток по умолчанию, связанный с объектом **Запись,** когда запись открыта, чтобы исключить круговую поездку только для открытия потока. </span><span class="sxs-lookup"><span data-stu-id="82429-112">You can obtain the default stream associated with a **Record** object when the **Record** is opened, to eliminate a round-trip just to open the stream.</span></span>

  - <span data-ttu-id="82429-113">Моментирование объекта **Stream.**</span><span class="sxs-lookup"><span data-stu-id="82429-113">By instantiating a **Stream** object.</span></span> <span data-ttu-id="82429-114">Эти **объекты Stream** можно использовать для хранения данных для целей приложения.</span><span class="sxs-lookup"><span data-stu-id="82429-114">These **Stream** objects can be used to store data for the purposes of your application.</span></span> <span data-ttu-id="82429-115">В отличие от **потока,** связанного  с URL-адресом или  потоком записи по **умолчанию,** мгновенный поток по умолчанию не имеет связи с исходным источником по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="82429-115">Unlike a **Stream** associated with a URL, or the default **Stream** of a **Record**, an instantiated **Stream** has no association with an underlying source by default.</span></span>

<span data-ttu-id="82429-116">С помощью методов и свойств объекта **Stream** можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="82429-116">With the methods and properties of a **Stream** object, you can do the following:</span></span>

  - <span data-ttu-id="82429-117">Откройте объект **Stream** из **записи** или URL-адреса методом [Open.](open-method-ado-stream.md)</span><span class="sxs-lookup"><span data-stu-id="82429-117">Open a **Stream** object from a **Record** or URL with the [Open](open-method-ado-stream.md) method.</span></span>

  - <span data-ttu-id="82429-118">Закрой **поток** [методом Close.](close-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="82429-118">Close a **Stream** with the [Close](close-method-ado.md) method.</span></span>

  - <span data-ttu-id="82429-119">Ввод bytes или text to a **Stream** с помощью методов [Write](write-method-ado.md) и [WriteText.](writetext-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="82429-119">Input bytes or text to a **Stream** with the [Write](write-method-ado.md) and [WriteText](writetext-method-ado.md) methods.</span></span>

  - <span data-ttu-id="82429-120">Чтение bytes из **потока** с помощью методов [Чтение](read-method-ado.md) и [ReadText.](readtext-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="82429-120">Read bytes from the **Stream** with the [Read](read-method-ado.md) and [ReadText](readtext-method-ado.md) methods.</span></span>

  - <span data-ttu-id="82429-121">**Записывайте все данные Потока** в буфере ADO на объект с помощью метода [Flush.](flush-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="82429-121">Write any **Stream** data still in the ADO buffer to the underlying object with the [Flush](flush-method-ado.md) method.</span></span>

  - <span data-ttu-id="82429-122">Скопируйте содержимое потока в  другой **поток** с помощью метода [CopyTo.](copyto-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="82429-122">Copy the contents of a **Stream** to another **Stream** with the [CopyTo](copyto-method-ado.md) method.</span></span>

  - <span data-ttu-id="82429-123">Управление чтением строк из исходных файлов с помощью метода [SkipLine](skipline-method-ado.md) и [свойства LineSeparator.](lineseparator-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="82429-123">Control how lines are read from the source file with the [SkipLine](skipline-method-ado.md) method and the [LineSeparator](lineseparator-property-ado.md) property.</span></span>

  - <span data-ttu-id="82429-124">Определите конец положения потока с помощью [свойства EOS](eos-property-ado.md) и [метода SetEOS.](seteos-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="82429-124">Determine the end of stream position with the [EOS](eos-property-ado.md) property and [SetEOS](seteos-method-ado.md) method.</span></span>

  - <span data-ttu-id="82429-125">Сохранение и восстановление данных в файлах с помощью [методов SaveToFile](savetofile-method-ado.md) и [LoadFromFile.](loadfromfile-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="82429-125">Save and restore data in files with the [SaveToFile](savetofile-method-ado.md) and [LoadFromFile](loadfromfile-method-ado.md) methods.</span></span>

  - <span data-ttu-id="82429-126">Укажите набор символов, используемый для хранения **потока** с [свойством Charset.](charset-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="82429-126">Specify the character set used for storing the **Stream** with the [Charset](charset-property-ado.md) property.</span></span>

  - <span data-ttu-id="82429-127">Остановите операцию асинхронного **потока** с помощью метода [Отмена.](cancel-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="82429-127">Halt an asynchronous **Stream** operation with the [Cancel](cancel-method-ado.md) method.</span></span>

  - <span data-ttu-id="82429-128">Определите количество bytes в **потоке** с [свойством Size.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream)</span><span class="sxs-lookup"><span data-stu-id="82429-128">Determine the number of bytes in a **Stream** with the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) property.</span></span>

  - <span data-ttu-id="82429-129">Управление текущей позицией в **потоке** с помощью [свойства Position.](position-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="82429-129">Control the current position within a **Stream** with the [Position](position-property-ado.md) property.</span></span>

  - <span data-ttu-id="82429-130">Определите тип данных в **потоке** с [свойством Type.](type-property-ado-stream.md)</span><span class="sxs-lookup"><span data-stu-id="82429-130">Determine the type of data in a **Stream** with the [Type](type-property-ado-stream.md) property.</span></span>

  - <span data-ttu-id="82429-131">Определите текущее состояние **потока** (закрытого, открытого или исполняемого) с [государственным свойством.](state-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="82429-131">Determine the current state of the **Stream** (closed, open, or executing) with the [State](state-property-ado.md) property.</span></span>

  - <span data-ttu-id="82429-132">Укажите режим доступа для **потока с** [свойством Mode.](mode-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="82429-132">Specify the access mode for the **Stream** with the [Mode](mode-property-ado.md) property.</span></span>

> [!NOTE]
> <span data-ttu-id="82429-133">URL-адреса, использующие схему http, автоматически вызывают поставщика DB Microsoft [OLE для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md)</span><span class="sxs-lookup"><span data-stu-id="82429-133">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="82429-134">Дополнительные сведения см. в [url-адресах Absolute и relative.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="82429-134">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


