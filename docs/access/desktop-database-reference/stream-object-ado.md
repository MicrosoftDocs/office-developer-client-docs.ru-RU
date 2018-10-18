---
title: Stream Object (ADO)
TOCTitle: Stream Object (ADO)
ms:assetid: d49b1514-e0b4-0aca-d5c2-8266f3f4fe65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250065(v=office.15)
ms:contentKeyID: 48547945
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f0a5ad4b50ed0548bad1f9a5482ee6755ecc9e2c
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603597"
---
# <a name="stream-object-ado"></a><span data-ttu-id="d06fc-102">Stream Object (ADO)</span><span class="sxs-lookup"><span data-stu-id="d06fc-102">Stream Object (ADO)</span></span>


<span data-ttu-id="d06fc-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d06fc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d06fc-104">Представляет поток двоичных данных или текст.</span><span class="sxs-lookup"><span data-stu-id="d06fc-104">Represents a stream of binary data or text.</span></span>

## <a name="remarks"></a><span data-ttu-id="d06fc-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="d06fc-105">Remarks</span></span>

<span data-ttu-id="d06fc-106">В структурированной дерева иерархии в файловой системе или систему электронной почты, [записи](record-object-ado.md) могут иметь по умолчанию двоичный поток битов, связанные с ним, содержащий содержимое файла или по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="d06fc-106">In tree-structured hierarchies such as a file system or an e-mail system, a [Record](record-object-ado.md) may have a default binary stream of bits associated with it that contains the contents of the file or the e-mail.</span></span> <span data-ttu-id="d06fc-107">Объект **потока** можно использовать для управления полей или записей, содержащих эти потоки данных.</span><span class="sxs-lookup"><span data-stu-id="d06fc-107">A **Stream** object can be used to manipulate fields or records containing these streams of data.</span></span> <span data-ttu-id="d06fc-108">Объект **потока** можно получить следующими способами:</span><span class="sxs-lookup"><span data-stu-id="d06fc-108">A **Stream** object can be obtained in these ways:</span></span>

  - <span data-ttu-id="d06fc-109">URL-адреса, с указанием объекта (обычно-файл), содержащего двоичные или текстовые данные.</span><span class="sxs-lookup"><span data-stu-id="d06fc-109">From a URL pointing to an object (typically a file) containing binary or text data.</span></span> <span data-ttu-id="d06fc-110">Этот объект может быть простой документ объект **записи** , представляющий структурированных документов или папку.</span><span class="sxs-lookup"><span data-stu-id="d06fc-110">This object can be a simple document, a **Record** object representing a structured document, or a folder.</span></span>

  - <span data-ttu-id="d06fc-111">Открыв объект **Stream** , связанной с объектом **записи** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d06fc-111">By opening the default **Stream** object associated with a **Record** object.</span></span> <span data-ttu-id="d06fc-112">Вы можете получить потока по умолчанию, связанного с объектом **записи** при открытии **записи** , чтобы избежать работа с форматом только для открытия в потоке.</span><span class="sxs-lookup"><span data-stu-id="d06fc-112">You can obtain the default stream associated with a **Record** object when the **Record** is opened, to eliminate a round-trip just to open the stream.</span></span>

  - <span data-ttu-id="d06fc-113">Путем создания экземпляра объекта **потока** .</span><span class="sxs-lookup"><span data-stu-id="d06fc-113">By instantiating a **Stream** object.</span></span> <span data-ttu-id="d06fc-114">Эти объекты **потока** можно использовать для хранения данных в рамках приложения.</span><span class="sxs-lookup"><span data-stu-id="d06fc-114">These **Stream** objects can be used to store data for the purposes of your application.</span></span> <span data-ttu-id="d06fc-115">В отличие от **потока** связанного с URL-адрес или **потока** **записи**по умолчанию инициализированный **потока** не связан ни с базовым источником по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d06fc-115">Unlike a **Stream** associated with a URL, or the default **Stream** of a **Record**, an instantiated **Stream** has no association with an underlying source by default.</span></span>

<span data-ttu-id="d06fc-116">С помощью методов и свойств объекта **потока** сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="d06fc-116">With the methods and properties of a **Stream** object, you can do the following:</span></span>

  - <span data-ttu-id="d06fc-117">Откройте объект **потока** из **записи** или URL-адрес с помощью метода [Open](open-method-ado-stream.md) .</span><span class="sxs-lookup"><span data-stu-id="d06fc-117">Open a **Stream** object from a **Record** or URL with the [Open](open-method-ado-stream.md) method.</span></span>

  - <span data-ttu-id="d06fc-118">Закройте **потока** с помощью метода [Close](close-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d06fc-118">Close a **Stream** with the [Close](close-method-ado.md) method.</span></span>

  - <span data-ttu-id="d06fc-119">Ввод: байт или текст **потока** с методами [создания](write-method-ado.md) и [WriteText](writetext-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d06fc-119">Input bytes or text to a **Stream** with the [Write](write-method-ado.md) and [WriteText](writetext-method-ado.md) methods.</span></span>

  - <span data-ttu-id="d06fc-120">Чтение байт **потока** с помощью методов [чтения](read-method-ado.md) и [ReadText](readtext-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d06fc-120">Read bytes from the **Stream** with the [Read](read-method-ado.md) and [ReadText](readtext-method-ado.md) methods.</span></span>

  - <span data-ttu-id="d06fc-121">Написание любой **поток** данных ADO буфера базового объекта с помощью метода [очистки](flush-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d06fc-121">Write any **Stream** data still in the ADO buffer to the underlying object with the [Flush](flush-method-ado.md) method.</span></span>

  - <span data-ttu-id="d06fc-122">Скопируйте содержимое **потока** с помощью метода [CopyTo](copyto-method-ado.md) другого **потока** .</span><span class="sxs-lookup"><span data-stu-id="d06fc-122">Copy the contents of a **Stream** to another **Stream** with the [CopyTo](copyto-method-ado.md) method.</span></span>

  - <span data-ttu-id="d06fc-123">Определяют, как читать строки из исходного файла с помощью метода [SkipLine](skipline-method-ado.md) и свойство [LineSeparator](lineseparator-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d06fc-123">Control how lines are read from the source file with the [SkipLine](skipline-method-ado.md) method and the [LineSeparator](lineseparator-property-ado.md) property.</span></span>

  - <span data-ttu-id="d06fc-124">Определение конечных положение потока с [EOS](eos-property-ado.md) свойство и метод [SetEOS](seteos-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d06fc-124">Determine the end of stream position with the [EOS](eos-property-ado.md) property and [SetEOS](seteos-method-ado.md) method.</span></span>

  - <span data-ttu-id="d06fc-125">Сохранения и восстановления данных в файлах с помощью методов [SaveToFile](savetofile-method-ado.md) и [LoadFromFile](loadfromfile-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d06fc-125">Save and restore data in files with the [SaveToFile](savetofile-method-ado.md) and [LoadFromFile](loadfromfile-method-ado.md) methods.</span></span>

  - <span data-ttu-id="d06fc-126">Укажите набор знаков, используемый для хранения **потока** со свойством [набор символов](charset-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d06fc-126">Specify the character set used for storing the **Stream** with the [Charset](charset-property-ado.md) property.</span></span>

  - <span data-ttu-id="d06fc-127">Остановка асинхронной операции **потока** с помощью метода [Отменить](cancel-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d06fc-127">Halt an asynchronous **Stream** operation with the [Cancel](cancel-method-ado.md) method.</span></span>

  - <span data-ttu-id="d06fc-128">Определение числа байтов **потока** с помощью свойства [размера](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="d06fc-128">Determine the number of bytes in a **Stream** with the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) property.</span></span>

  - <span data-ttu-id="d06fc-129">Элемент управления текущей позиции в **потоке** со свойством [положение](position-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d06fc-129">Control the current position within a **Stream** with the [Position](position-property-ado.md) property.</span></span>

  - <span data-ttu-id="d06fc-130">Определение типа данных в **поток** со свойством [типа](type-property-ado-stream.md) .</span><span class="sxs-lookup"><span data-stu-id="d06fc-130">Determine the type of data in a **Stream** with the [Type](type-property-ado-stream.md) property.</span></span>

  - <span data-ttu-id="d06fc-131">Определите текущее состояние **потока** (закрытой, open или выполнения) с помощью свойства [состояний](state-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d06fc-131">Determine the current state of the **Stream** (closed, open, or executing) with the [State](state-property-ado.md) property.</span></span>

  - <span data-ttu-id="d06fc-132">Задать режим доступа для **потока** с помощью свойства [режима](mode-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d06fc-132">Specify the access mode for the **Stream** with the [Mode](mode-property-ado.md) property.</span></span>

<span data-ttu-id="d06fc-133"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="d06fc-133"><<<<<<< HEAD</span></span>

> [!NOTE]
> <P><span data-ttu-id="d06fc-134">URL-адреса, с помощью схемы http автоматически вызывает <A href="microsoft-ole-db-provider-for-internet-publishing.md">Поставщик Microsoft OLE DB для публикации Интернет</A>.</span><span class="sxs-lookup"><span data-stu-id="d06fc-134">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>.</span></span> <span data-ttu-id="d06fc-135">Для получения дополнительных сведений см <A href="absolute-and-relative-urls.md">абсолютного и относительных URL-адресов</A>.</span><span class="sxs-lookup"><span data-stu-id="d06fc-135">For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> [!NOTE]
> <span data-ttu-id="d06fc-136">URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="d06fc-136">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="d06fc-137">Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="d06fc-137">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="d06fc-138">master</span><span class="sxs-lookup"><span data-stu-id="d06fc-138">master</span></span>


