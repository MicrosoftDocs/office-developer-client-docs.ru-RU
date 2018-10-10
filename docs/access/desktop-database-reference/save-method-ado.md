---
title: Метод - Save ActiveX Data Objects (ADO)
TOCTitle: Save Method (ADO)
ms:assetid: 02dab13b-f947-b96d-46ea-0def3ed8f28f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248793(v=office.15)
ms:contentKeyID: 48542968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd77102d178399afeb3ebcb493799e83467c4687
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483066"
---
# <a name="save-method-ado"></a><span data-ttu-id="52311-102">Save Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="52311-102">Save Method (ADO)</span></span>


<span data-ttu-id="52311-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="52311-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="52311-104">Сохранение [набора записей](recordset-object-ado.md) в файл или объект [Stream](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="52311-104">Saves the [Recordset](recordset-object-ado.md) in a file or [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="52311-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52311-105">Syntax</span></span>

<span data-ttu-id="52311-106">*набор записей*. Сохранение*назначения*, *PersistFormat*</span><span class="sxs-lookup"><span data-stu-id="52311-106">*recordset*.Save*Destination*, *PersistFormat*</span></span>

## <a name="parameters"></a><span data-ttu-id="52311-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="52311-107">Parameters</span></span>

  - <span data-ttu-id="52311-108">*Назначения*</span><span class="sxs-lookup"><span data-stu-id="52311-108">*Destination*</span></span>

  - <span data-ttu-id="52311-109">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="52311-109">Optional.</span></span> <span data-ttu-id="52311-110">**Variant** , представляющий полный путь файла, в которых будут сохраняться **записей** или ссылку на объект **Stream** .</span><span class="sxs-lookup"><span data-stu-id="52311-110">A **Variant** that represents the complete path name of the file where the **Recordset** is to be saved, or a reference to a **Stream** object.</span></span>

  - <span data-ttu-id="52311-111">*PersistFormat*</span><span class="sxs-lookup"><span data-stu-id="52311-111">*PersistFormat*</span></span>

  - <span data-ttu-id="52311-112">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="52311-112">Optional.</span></span> <span data-ttu-id="52311-113">[PersistFormatEnum](persistformatenum.md) значение, указывающее формат, в котором должен быть сохранен (XML или ADTG) **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="52311-113">A [PersistFormatEnum](persistformatenum.md) value that specifies the format in which the **Recordset** is to be saved (XML or ADTG).</span></span> <span data-ttu-id="52311-114">Значение по умолчанию — **adPersistADTG**.</span><span class="sxs-lookup"><span data-stu-id="52311-114">The default value is **adPersistADTG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="52311-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="52311-115">Remarks</span></span>

<span data-ttu-id="52311-116">Метод **Save** можно вызвать только на открытие **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="52311-116">The **Save** method can only be invoked on an open **Recordset**.</span></span> <span data-ttu-id="52311-117">Используйте метод [Open](open-method-ado-recordset.md) позднее восстановление **набора записей** из *места назначения*.</span><span class="sxs-lookup"><span data-stu-id="52311-117">Use the [Open](open-method-ado-recordset.md) method to later restore the **Recordset** from *Destination*.</span></span>

<span data-ttu-id="52311-118">Если **записей**не свойство [фильтра](filter-property-ado.md) , будут сохранены только строки, доступных в группе фильтр.</span><span class="sxs-lookup"><span data-stu-id="52311-118">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, then only the rows accessible under the filter are saved.</span></span> <span data-ttu-id="52311-119">Если иерархических **записей** , затем дочерние текущего **набора записей** и его дочерние элементы сохраняются, включая родительского **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="52311-119">If the **Recordset** is hierarchical, then the current child **Recordset** and its children are saved, including the parent **Recordset**.</span></span> <span data-ttu-id="52311-120">Метод **Save** дочернего вызванный **записей** , дочерних и все его дочерние элементы сохраняются, но родительский не.</span><span class="sxs-lookup"><span data-stu-id="52311-120">If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not.</span></span>

<span data-ttu-id="52311-121">При первом сохранении **набора записей**, он не является обязательным для указания *назначения*.</span><span class="sxs-lookup"><span data-stu-id="52311-121">The first time you save the **Recordset**, it is optional to specify *Destination*.</span></span> <span data-ttu-id="52311-122">Если параметр *результат*не задан, будет создан новый файл с именем, задайте значение свойства [источника](source-property-ado-recordset.md) **записей**.</span><span class="sxs-lookup"><span data-stu-id="52311-122">If you omit *Destination*, a new file will be created with a name set to the value of the [Source](source-property-ado-recordset.md) property of the **Recordset**.</span></span>

<span data-ttu-id="52311-123">Параметр *результат* не задан, при последовательном вызове **Сохранить** после первого сохранить или произойдет ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="52311-123">Omit *Destination* when you subsequently call **Save** after the first save, or a run-time error will occur.</span></span> <span data-ttu-id="52311-124">При последующем вызове **Сохранить** с нового *назначения*, **записей** сохраняется в новое место назначения.</span><span class="sxs-lookup"><span data-stu-id="52311-124">If you subsequently call **Save** with a new *Destination*, the **Recordset** is saved to the new destination.</span></span> <span data-ttu-id="52311-125">Тем не менее новые назначения и конечный оба будет открыть.</span><span class="sxs-lookup"><span data-stu-id="52311-125">However, the new destination and the original destination will both be open.</span></span>

<span data-ttu-id="52311-126">**Сохранить** не закрывается **записей** или *назначения*, поэтому можно продолжать работать с **набора записей** и сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="52311-126">**Save** does not close the **Recordset** or *Destination*, so you can continue to work with the **Recordset** and save your most recent changes.</span></span> <span data-ttu-id="52311-127">*Назначение* остается открытым до закрытия **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="52311-127">*Destination* remains open until the **Recordset** is closed.</span></span>

<span data-ttu-id="52311-128">По соображениям безопасности метод **Save** разрешает использование безопасности низкой и пользовательские параметры из сценарий, выполняемый с Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="52311-128">For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer.</span></span> <span data-ttu-id="52311-129">Более подробное описание проблемы безопасности в разделе «ADO и RDS безопасности проблемы в Microsoft Internet Explorer» в разделе ActiveX Data Objects (ADO) технические статьи в технические статьи доступа к данным Microsoft.</span><span class="sxs-lookup"><span data-stu-id="52311-129">For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span></span>

<span data-ttu-id="52311-130">Если метод **Save** вызывается при асинхронное извлечение **записей** , execute или обновить операция находится в стадии разработки, а затем **Сохраните** ожидает до завершения асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="52311-130">If the **Save** method is called while an asynchronous **Recordset** fetch, execute, or update operation is in progress, then **Save** waits until the asynchronous operation is complete.</span></span>

<span data-ttu-id="52311-131">Записи сохраняются, начиная с первой строки текущего **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="52311-131">Records are saved beginning with the first row of the **Recordset**.</span></span> <span data-ttu-id="52311-132">После завершения метода **Save** первой строки текущего **набора записей**перемещаются текущей позиции строки.</span><span class="sxs-lookup"><span data-stu-id="52311-132">When the **Save** method is finished, the current row position is moved to the first row of the **Recordset**.</span></span>

<span data-ttu-id="52311-133">Для достижения наилучших результатов присвойте свойству [CursorLocation](cursorlocation-property-ado.md) значение **adUseClient** с **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="52311-133">For best results, set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** with **Save**.</span></span> <span data-ttu-id="52311-134">Если ваш поставщик поддерживает все функциональные возможности, необходимые для сохранения **записей** объекты, службы курсора будет предоставлять функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="52311-134">If your provider does not support all of the functionality necessary to save **Recordset** objects, the Cursor Service will provide that functionality.</span></span>

<span data-ttu-id="52311-135">После сохранения **записей** со свойством **CursorLocation** , задайте значение **adUseServer**ограничено возможность обновления для **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="52311-135">When a **Recordset** is persisted with the **CursorLocation** property set to **adUseServer**, the update capability for the **Recordset** is limited.</span></span> <span data-ttu-id="52311-136">Как правило только для одной таблицы обновления, вставки и удаления могут (зависит от функциональности поставщика).</span><span class="sxs-lookup"><span data-stu-id="52311-136">Typically, only single-table updates, insertions, and deletions are allowed (dependant upon provider functionality).</span></span> <span data-ttu-id="52311-137">Метод [выполнить повторную синхронизацию](resync-method-ado.md) также недоступен в этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="52311-137">The [Resync](resync-method-ado.md) method is also unavailable in this configuration.</span></span>


> [!NOTE]
> <P><span data-ttu-id="52311-138">Сохранение <STRONG>набора записей</STRONG> с <STRONG>полей</STRONG> типа <STRONG>adVariant</STRONG>, <STRONG>adIDispatch</STRONG>или <STRONG>adIUnknown</STRONG> ADO не поддерживается и может привести к непредсказуемым последствиям.</span><span class="sxs-lookup"><span data-stu-id="52311-138">Saving a <STRONG>Recordset</STRONG> with <STRONG>Fields</STRONG> of type <STRONG>adVariant</STRONG>, <STRONG>adIDispatch</STRONG>, or <STRONG>adIUnknown</STRONG> is not supported by ADO and can cause unpredictable results.</span></span></P>



<span data-ttu-id="52311-139">Только **фильтры** в виде строки критерии (например OrderDate \> "12/31/1999") влияет на содержимое постоянных **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="52311-139">Only **Filters** in the form of Criteria Strings (e.g. OrderDate \> '12/31/1999') affect the contents of a persisted **Recordset**.</span></span> <span data-ttu-id="52311-140">Фильтры, созданные с помощью массива **закладки** или с использованием значения из **FilterGroupEnum** не влияет на содержимое постоянных **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="52311-140">Filters created with an Array of **Bookmarks** or using a value from the **FilterGroupEnum** will not affect the contents of the persisted **Recordset**.</span></span> <span data-ttu-id="52311-141">Эти правила применяются к **наборов записей** , созданных с помощью курсоры со стороны клиента или на сервере.</span><span class="sxs-lookup"><span data-stu-id="52311-141">These rules apply to **Recordsets** created with either client-side or server-side cursors.</span></span>

<span data-ttu-id="52311-142">Так как параметр *назначения* может принимать любой объект, который поддерживает интерфейс OLE DB IStream, можно сохранить **записей** непосредственно к объекту ASP ответа.</span><span class="sxs-lookup"><span data-stu-id="52311-142">Because the *Destination* parameter can accept any object that supports the OLE DB IStream interface, you can save a **Recordset** directly to the ASP Response object.</span></span> <span data-ttu-id="52311-143">Дополнительные сведения можно найти в [Сценарии хранение записей XML](xml-recordset-persistence-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="52311-143">For more details, please see the [XML Recordset Persistence Scenario](xml-recordset-persistence-scenario.md).</span></span>

<span data-ttu-id="52311-144">Можно также сохранить **набора записей** в формате XML в экземпляр объекта MSXML DOM, как показано в следующем коде Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="52311-144">You can also save a **Recordset** in XML format to an instance of an MSXML DOM object, as is shown in the following Visual Basic code:</span></span>


> [!NOTE]
> <P><span data-ttu-id="52311-145">Два ограничения при сохранении иерархические <STRONG>наборы записей</STRONG> (данные фигуры) в формате XML.</span><span class="sxs-lookup"><span data-stu-id="52311-145">Two limitations apply when saving hierarchical <STRONG>Recordsets</STRONG> (data shapes) in XML format.</span></span> <span data-ttu-id="52311-146">Не удается сохранить в XML, если иерархических <STRONG>записей</STRONG> содержит ожидающие обновления и не могут сохранять параметризованный иерархических <STRONG>набора записей</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="52311-146">You cannot save into XML if the hierarchical <STRONG>Recordset</STRONG> contains pending updates, and you cannot save a parameterized hierarchical <STRONG>Recordset</STRONG>.</span></span></P>



<span data-ttu-id="52311-147">Записей, сохраненных в формате XML сохраняется в формате UTF-8.</span><span class="sxs-lookup"><span data-stu-id="52311-147">A Recordset saved in XML format is saved using UTF-8 format.</span></span> <span data-ttu-id="52311-148">При такой файл загружается в ADO Stream, объект Stream не будет предпринята попытка открытия набора записей в потоке, если свойство Charset потока не установлен в соответствующее значение формат UTF-8.</span><span class="sxs-lookup"><span data-stu-id="52311-148">When such a file is loaded into an ADO Stream, the Stream object will not attempt to open a Recordset from the stream unless the Charset property of the stream is set to the appropriate value for UTF-8 format.</span></span>

