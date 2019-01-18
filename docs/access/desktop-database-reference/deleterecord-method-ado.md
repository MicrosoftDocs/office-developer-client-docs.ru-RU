---
title: Метод DeleteRecord (ADO)
TOCTitle: DeleteRecord method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d6ecd408bc2141ef9ff4bec8f6469a70e09bbe1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704520"
---
# <a name="deleterecord-method-ado"></a><span data-ttu-id="5aa80-102">Метод DeleteRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="5aa80-102">DeleteRecord method (ADO)</span></span>

<span data-ttu-id="5aa80-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5aa80-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5aa80-104">Удаляет сущности, представленной в [записи](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5aa80-104">Deletes a the entity represented by a [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa80-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5aa80-105">Syntax</span></span>

<span data-ttu-id="5aa80-106">*Запись*. \**макрокоманду УдалитьЗапись \*\*\* источника*, *Async*</span><span class="sxs-lookup"><span data-stu-id="5aa80-106">*Record*.\**DeleteRecord\*\*\*Source*, *Async*</span></span>

## <a name="parameters"></a><span data-ttu-id="5aa80-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="5aa80-107">Parameters</span></span>

|<span data-ttu-id="5aa80-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="5aa80-108">Parameter</span></span>|<span data-ttu-id="5aa80-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5aa80-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5aa80-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="5aa80-110">*Source*</span></span> |<span data-ttu-id="5aa80-111">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="5aa80-111">Optional.</span></span> <span data-ttu-id="5aa80-112">**Строковое** значение, содержащее URL-адрес определение сущности (например, файл или каталог) для удаления.</span><span class="sxs-lookup"><span data-stu-id="5aa80-112">A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted.</span></span> <span data-ttu-id="5aa80-113">Если *источник* указан или указывает пустая строка, удаляется сущности, представленной текущей [записи](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="5aa80-113">If *Source* is omitted or specifies an empty string, the entity represented by the current [Record](record-object-ado.md) is deleted.</span></span> <span data-ttu-id="5aa80-114">Если запись является записью семейства сайтов ([типом записи](recordtype-property-ado.md) из **adCollectionRecord**, такие как каталог) также будут удалены все дочерние элементы (например, вложенные папки).</span><span class="sxs-lookup"><span data-stu-id="5aa80-114">If the Record is a collection record ([RecordType](recordtype-property-ado.md) of **adCollectionRecord**, such as a directory) all children (for example, subdirectories) will also be deleted.</span></span>|
|<span data-ttu-id="5aa80-115">*Async*</span><span class="sxs-lookup"><span data-stu-id="5aa80-115">*Async*</span></span> |<span data-ttu-id="5aa80-116">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="5aa80-116">Optional.</span></span> <span data-ttu-id="5aa80-117">**Логическое** значение, которое, если **значение True**, указывает, что асинхронной операции удаления.</span><span class="sxs-lookup"><span data-stu-id="5aa80-117">A **Boolean** value that, when **True**, specifies that the delete operation is asynchronous.</span></span>|

## <a name="remarks"></a><span data-ttu-id="5aa80-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="5aa80-118">Remarks</span></span>

<span data-ttu-id="5aa80-119">Операции на объект, представленный этой **записи** могут завершиться с ошибкой после завершения этого метода.</span><span class="sxs-lookup"><span data-stu-id="5aa80-119">Operations on the object represented by this **Record** may fail after this method completes.</span></span> <span data-ttu-id="5aa80-120">После вызова **макрокоманду УдалитьЗапись** **записи** должны быть закрыты, так как поведение **записи** могут стать непредсказуемое в зависимости от, когда поставщик обновляет **запись** с источником данных.</span><span class="sxs-lookup"><span data-stu-id="5aa80-120">After calling **DeleteRecord**, the **Record** should be closed because the behavior of the **Record** may become unpredictable depending upon when the provider updates the **Record** with the data source.</span></span>

<span data-ttu-id="5aa80-121">Если эта **запись** был получен из [набора записей](recordset-object-ado.md), затем результаты этой операции будет не будут отражены сразу же в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="5aa80-121">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="5aa80-122">Обновление **набора записей** , закрыть и повторно открыть его или выполнив методы **записей** [запроса](requery-method-ado.md)или [обновления](update-method-ado.md) и [выполнить повторную синхронизацию](resync-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="5aa80-122">Refresh the **Recordset** by closing and re-opening it, or by executing the **Recordset** [Requery](requery-method-ado.md), or [Update](update-method-ado.md) and [Resync](resync-method-ado.md) methods.</span></span>

> [!NOTE]
> <span data-ttu-id="5aa80-123">URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="5aa80-123">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="5aa80-124">Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="5aa80-124">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


