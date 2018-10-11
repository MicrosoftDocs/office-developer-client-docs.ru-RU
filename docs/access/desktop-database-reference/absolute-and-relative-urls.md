---
title: Absolute and Relative URLs
TOCTitle: Absolute and Relative URLs
ms:assetid: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15)
ms:contentKeyID: 48545774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bc0cb3086f8fdfa032c005f7e2d219dab56999b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482528"
---
# <a name="absolute-and-relative-urls"></a><span data-ttu-id="78c32-102">Absolute and Relative URLs</span><span class="sxs-lookup"><span data-stu-id="78c32-102">Absolute and Relative URLs</span></span>

<span data-ttu-id="78c32-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="78c32-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="78c32-104">URL-адрес указывает расположение целевого, хранящиеся на компьютере локальный или сетевой, такие как файл, каталог, HTML-страницу, изображения, программы и т. п.*.*</span><span class="sxs-lookup"><span data-stu-id="78c32-104">A URL specifies the location of a target stored on a local or networked computer, such as a file, directory, HTML page, image, program, and so on *.*</span></span> <span data-ttu-id="78c32-105">В этом разделе рассмотрена *абсолютный URL-адрес* имеет вид:</span><span class="sxs-lookup"><span data-stu-id="78c32-105">In this discussion, an *absolute URL* is of the form:</span></span>

<span data-ttu-id="78c32-106">*Scheme://Server/Path/Resource*</span><span class="sxs-lookup"><span data-stu-id="78c32-106">*scheme://server/path/resource*</span></span>

<span data-ttu-id="78c32-107">где:</span><span class="sxs-lookup"><span data-stu-id="78c32-107">where:</span></span>

  - <span data-ttu-id="78c32-108">*Схема*</span><span class="sxs-lookup"><span data-stu-id="78c32-108">*scheme*</span></span>

  - <span data-ttu-id="78c32-109">Определяет, как получить доступ к *ресурсов* .</span><span class="sxs-lookup"><span data-stu-id="78c32-109">Specifies how the *resource* is to be accessed.</span></span>

  - <span data-ttu-id="78c32-110">*server*</span><span class="sxs-lookup"><span data-stu-id="78c32-110">*server*</span></span>

  - <span data-ttu-id="78c32-111">Задает имя компьютера, где находится *ресурсов* .</span><span class="sxs-lookup"><span data-stu-id="78c32-111">Specifies the name of the computer where the *resource* is located.</span></span>

  - <span data-ttu-id="78c32-112">*путь*</span><span class="sxs-lookup"><span data-stu-id="78c32-112">*path*</span></span>

  - <span data-ttu-id="78c32-113">Определяет последовательность каталоги, приводя к целевой объект.</span><span class="sxs-lookup"><span data-stu-id="78c32-113">Specifies the sequence of directories leading to the target.</span></span> <span data-ttu-id="78c32-114">Если *ресурс* задан, целевой объект является последнего каталога в *пути*.</span><span class="sxs-lookup"><span data-stu-id="78c32-114">If *resource* is omitted, the target is the last directory in *path*.</span></span>

  - <span data-ttu-id="78c32-115">*resource*</span><span class="sxs-lookup"><span data-stu-id="78c32-115">*resource*</span></span>

  - <span data-ttu-id="78c32-116">Если включен, *ресурсов* является целевым и как правило, имя файла.</span><span class="sxs-lookup"><span data-stu-id="78c32-116">If included, *resource* is the target, and is typically the name of a file.</span></span> <span data-ttu-id="78c32-117">Может быть *простой файл* , содержащий один поток двоичных байтов или *структурированных документов* , содержащий один или несколько хранилищ и двоичных потоков в байтах.</span><span class="sxs-lookup"><span data-stu-id="78c32-117">It may be a *simple file,* containing a single binary stream of bytes, or a *structured document,* containing one or more storages and binary streams of bytes.</span></span>

<span data-ttu-id="78c32-118">*Абсолютный URL-адрес* содержит все сведения, необходимые для размещения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78c32-118">An *absolute URL* contains all the information necessary to locate a resource.</span></span>

<span data-ttu-id="78c32-119">*Относительный URL-адрес* поиск ресурсов, используя абсолютный URL-адрес в качестве отправной точки.</span><span class="sxs-lookup"><span data-stu-id="78c32-119">A *relative URL* locates a resource using an absolute URL as a starting point.</span></span> <span data-ttu-id="78c32-120">В результате «полный URL-адрес» конечного объекта указывается, объединив абсолютных и относительных URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="78c32-120">In effect, the "complete URL" of the target is specified by concatenating the absolute and relative URLs.</span></span> <span data-ttu-id="78c32-121">Относительный URL-адрес обычно состоит только из *пути*и, при необходимости, *ресурсов*, но не *схему* или *сервера*.</span><span class="sxs-lookup"><span data-stu-id="78c32-121">A relative URL typically consists only of the *path*, and optionally, the *resource*, but no *scheme* or *server*.</span></span>

## <a name="url-scheme-registration"></a><span data-ttu-id="78c32-122">URL-адрес схемы регистрации</span><span class="sxs-lookup"><span data-stu-id="78c32-122">URL Scheme Registration</span></span>

<span data-ttu-id="78c32-123">Если поставщик поддерживает URL-адреса, он будет зарегистрирован для одного или нескольких URL-адрес схемы.</span><span class="sxs-lookup"><span data-stu-id="78c32-123">If a provider supports URLs, it will register for one or more URL schemes.</span></span> <span data-ttu-id="78c32-124">Это означает, что все URL-адреса, с помощью этой схемы автоматически вызывается зарегистрированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="78c32-124">This means that any URLs using this scheme will automatically invoke the registered provider.</span></span> <span data-ttu-id="78c32-125">Например схему *http* регистрируется [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="78c32-125">For example, the *http* scheme is registered to the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="78c32-126">ADO предполагается, что все URL-адреса, начинаются с «http» представляют веб-папок или файлов для использования с поставщиком публикации Интернет.</span><span class="sxs-lookup"><span data-stu-id="78c32-126">ADO assumes all URLs prefixed with "http" represent Web folders or files to be used with the Internet Publishing Provider.</span></span> <span data-ttu-id="78c32-127">Сведения о схемы, зарегистрированные поставщиком обратитесь к документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="78c32-127">For information about the schemes registered by your provider, see your provider documentation.</span></span>

## <a name="defining-context-with-a-url"></a><span data-ttu-id="78c32-128">Определение контекста с URL-адреса</span><span class="sxs-lookup"><span data-stu-id="78c32-128">Defining Context with a URL</span></span>

<span data-ttu-id="78c32-129">Одна функция открытое подключение, представленного объектом [подключения](connection-object-ado.md) — для ограничения последующих операций к источнику данных, представленного это подключение.</span><span class="sxs-lookup"><span data-stu-id="78c32-129">One function of an open connection, represented by a [Connection](connection-object-ado.md) object, is to restrict subsequent operations to the data source represented by that connection.</span></span> <span data-ttu-id="78c32-130">То есть подключение определяет контекст для последующих операций.</span><span class="sxs-lookup"><span data-stu-id="78c32-130">That is, the connection defines the context for subsequent operations.</span></span>

<span data-ttu-id="78c32-131">С помощью ADO 2.5 абсолютный URL-адрес может также определять контекст.</span><span class="sxs-lookup"><span data-stu-id="78c32-131">With ADO 2.5, an absolute URL may also define a context.</span></span> <span data-ttu-id="78c32-132">Например при [записи](record-object-ado.md) объекта открывается с абсолютный URL-адрес, объект **подключения** неявно создается для представления ресурса, указанного URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="78c32-132">For example, when a [Record](record-object-ado.md) object is opened with an absolute URL, a **Connection** object is implicitly created to represent the resource specified by the URL.</span></span>

<span data-ttu-id="78c32-133">Абсолютный URL-адрес, который определяет контекст может быть указано в параметре *ActiveConnection* метод [Open](open-method-ado-record.md) объекта **записи** .</span><span class="sxs-lookup"><span data-stu-id="78c32-133">An absolute URL that defines a context may be specified in the *ActiveConnection* parameter of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="78c32-134">Абсолютный URL-адрес также может быть указано как значение новой «URL-адрес**=**"ключевого слова в параметр *ConnectionString* [Open](open-method-ado-connection.md) метод **подключения** объекта и метод [Open](open-method-ado-recordset.md) \*ActiveConnection объекта [набора записей](recordset-object-ado.md) \*параметр.</span><span class="sxs-lookup"><span data-stu-id="78c32-134">An absolute URL may also be specified as the value of the new "URL**=**" keyword in the **Connection** object [Open](open-method-ado-connection.md) method *ConnectionString* parameter, and the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method *ActiveConnection* parameter.</span></span>

<span data-ttu-id="78c32-135">Контекст также может быть определен с помощью open объекта **записи** или **набора записей** , который представляет каталог, так как эти объекты уже явно или неявно объявленные объект **подключения** , который определяет контекст.</span><span class="sxs-lookup"><span data-stu-id="78c32-135">Context may also be defined with an open **Record** or **Recordset** object that represents a directory because these objects already have an implicitly or explicitly declared **Connection** object that specifies context.</span></span>

## <a name="scoped-operations"></a><span data-ttu-id="78c32-136">Операции с областью</span><span class="sxs-lookup"><span data-stu-id="78c32-136">Scoped Operations</span></span>

<span data-ttu-id="78c32-137">Контекст одновременно определяет *область* , то есть в каталоге и его подкаталогах, которые могут принимать участие в последующих операций.</span><span class="sxs-lookup"><span data-stu-id="78c32-137">The context simultaneously defines a *scope* — that is, the directory and its subdirectories that may participate in subsequent operations.</span></span> <span data-ttu-id="78c32-138">Объект **записи** имеет несколько заданной областью методов, включая [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md)и [макрокоманду УдалитьЗапись](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), работающих на каталог и все его подкаталоги.</span><span class="sxs-lookup"><span data-stu-id="78c32-138">The **Record** object has several scoped methods, including [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md), and [DeleteRecord](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), that operate on a directory and all its subdirectories.</span></span>

## <a name="relative-urls-as-command-text"></a><span data-ttu-id="78c32-139">Относительный URL-адреса как текст команды</span><span class="sxs-lookup"><span data-stu-id="78c32-139">Relative URLs as Command Text</span></span>

<span data-ttu-id="78c32-140">Строка, содержащая команду для выполнения в источнике данных может быть указано параметр *CommandText* метод **Execute** объекта **подключения** , а параметр **Open** *источника* метод **набора записей** объекта.</span><span class="sxs-lookup"><span data-stu-id="78c32-140">A string specifying a command to be executed on the data source may be specified in the **Connection** object **Execute** method *CommandText* parameter, and the **Recordset** object **Open** method *Source* parameter.</span></span>

<span data-ttu-id="78c32-141">Относительный URL-адрес может быть указано в параметре *CommandText* или *источника* .</span><span class="sxs-lookup"><span data-stu-id="78c32-141">A relative URL may be specified in the *CommandText* or *Source* parameter.</span></span> <span data-ttu-id="78c32-142">Относительный URL-адрес не указывает, команда (например, команды SQL); просто указывается в этих параметров.</span><span class="sxs-lookup"><span data-stu-id="78c32-142">The relative URL does not actually specify a command (such as an SQL command); it is merely specified in those parameters.</span></span> <span data-ttu-id="78c32-143">Кроме того контекст активного подключения должен быть абсолютный URL-адрес, а параметр *параметр* должен иметь значение **adCmdTableDirect**.</span><span class="sxs-lookup"><span data-stu-id="78c32-143">In addition, the context of the active connection must be an absolute URL, and the *Option* parameter must be set to **adCmdTableDirect**.</span></span>

<span data-ttu-id="78c32-144">Например, **набор записей** может быть открыт на файл Readme25.txt в каталоге Winnt/system32 следующим образом:</span><span class="sxs-lookup"><span data-stu-id="78c32-144">For example, a **Recordset** could be opened on the Readme25.txt file of the Winnt/system32 directory like this:</span></span>

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

<span data-ttu-id="78c32-145">Абсолютный URL-адрес в строку подключения указывает server (сервер) и (путь) и путь (Winnt).</span><span class="sxs-lookup"><span data-stu-id="78c32-145">The absolute URL in the connection string specifies the server (YourServer ) and the path () and the path (Winnt ).</span></span> <span data-ttu-id="78c32-146">Этот URL-адрес также определяет контекст.</span><span class="sxs-lookup"><span data-stu-id="78c32-146">This URL also defines the context.</span></span>

<span data-ttu-id="78c32-147">Относительный URL-адрес в текст команды использует абсолютный URL-адрес в качестве отправной точки и указывает в оставшейся части путь (system32) и файл, чтобы открыть () и файл, чтобы открыть (Readme25.txt).</span><span class="sxs-lookup"><span data-stu-id="78c32-147">The relative URL in the command text uses the absolute URL as a starting point and specifies the remainder of the path (system32 ) and the file to open () and the file to open (Readme25.txt ).</span></span>

<span data-ttu-id="78c32-148">Параметры (поле) указывает, что тип команды относительный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="78c32-148">The options field () indicates that the command type is a relative URL.</span></span>

<span data-ttu-id="78c32-149">Другой пример: следующий код откроется **записей** на содержимое каталога:</span><span class="sxs-lookup"><span data-stu-id="78c32-149">As another example, the following code will open a **Recordset** on the contents of the directory:</span></span>

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a><span data-ttu-id="78c32-150">Схемы URL-адрес, предоставленный поставщика OLE DB</span><span class="sxs-lookup"><span data-stu-id="78c32-150">OLE DB Provider-Supplied URL Schemes</span></span>

<span data-ttu-id="78c32-151">Начальная часть полный URL-адрес — это *Схема* , используемая для доступа к ресурсу, определяемому в оставшейся части URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="78c32-151">The leading part of a fully-qualified URL is the *scheme* used to access the resource identified by the remainder of the URL.</span></span> <span data-ttu-id="78c32-152">Примерами являются HTTP (HyperText Transfer Protocol) и FTP (протокол передачи файлов).</span><span class="sxs-lookup"><span data-stu-id="78c32-152">Examples are HTTP (HyperText Transfer Protocol) and FTP (File Transfer Protocol).</span></span>

<span data-ttu-id="78c32-153">ADO поддерживает поставщики OLE DB, распознает собственные схемы URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="78c32-153">ADO supports OLE DB providers that recognize their own URL schemes.</span></span> <span data-ttu-id="78c32-154">Например, [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md)*,* которых доступ «опубликованный» файлы Windows 2000, распознает существующую схему HTTP.</span><span class="sxs-lookup"><span data-stu-id="78c32-154">For example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses "published" Windows 2000 files, recognizes the existing HTTP scheme.</span></span>

