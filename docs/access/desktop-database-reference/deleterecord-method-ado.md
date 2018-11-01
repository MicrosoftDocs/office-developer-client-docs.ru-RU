---
title: Метод макрокоманду УдалитьЗапись (ADO)
TOCTitle: DeleteRecord Method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9dd9c5b6681732ec50442f7a4bcd9874ecf4e493
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878998"
---
# <a name="deleterecord-method-ado"></a><span data-ttu-id="17728-102">Метод макрокоманду УдалитьЗапись (ADO)</span><span class="sxs-lookup"><span data-stu-id="17728-102">DeleteRecord Method (ADO)</span></span>


<span data-ttu-id="17728-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="17728-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="17728-104">Удаляет сущности, представленной в [записи](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="17728-104">Deletes a the entity represented by a [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="17728-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17728-105">Syntax</span></span>

<span data-ttu-id="17728-106">*Запись*. \**макрокоманду УдалитьЗапись \*\*\* источника*, *Async*</span><span class="sxs-lookup"><span data-stu-id="17728-106">*Record*.\**DeleteRecord\*\*\*Source*, *Async*</span></span>

## <a name="parameters"></a><span data-ttu-id="17728-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="17728-107">Parameters</span></span>

  - <span data-ttu-id="17728-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="17728-108">*Source*</span></span>

  - <span data-ttu-id="17728-109">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="17728-109">Optional.</span></span> <span data-ttu-id="17728-110">**Строковое** значение, содержащее URL-адрес определение сущности (например, файл или каталог) для удаления.</span><span class="sxs-lookup"><span data-stu-id="17728-110">A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted.</span></span> <span data-ttu-id="17728-111">Если *источник* указан или указывает пустая строка, удаляется сущности, представленной текущей [записи](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="17728-111">If *Source* is omitted or specifies an empty string, the entity represented by the current [Record](record-object-ado.md) is deleted.</span></span> <span data-ttu-id="17728-112">Если запись является записью семейства сайтов ([типом записи](recordtype-property-ado.md) из **adCollectionRecord**, такие как каталог) также будут удалены все дочерние элементы (например, вложенные папки).</span><span class="sxs-lookup"><span data-stu-id="17728-112">If the Record is a collection record ([RecordType](recordtype-property-ado.md) of **adCollectionRecord**, such as a directory) all children (for example, subdirectories) will also be deleted.</span></span>

  - <span data-ttu-id="17728-113">*Async*</span><span class="sxs-lookup"><span data-stu-id="17728-113">*Async*</span></span>

  - <span data-ttu-id="17728-114">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="17728-114">Optional.</span></span> <span data-ttu-id="17728-115">**Логическое** значение, которое, если **значение True**, указывает, что асинхронной операции удаления.</span><span class="sxs-lookup"><span data-stu-id="17728-115">A **Boolean** value that, when **True**, specifies that the delete operation is asynchronous.</span></span>

## <a name="remarks"></a><span data-ttu-id="17728-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="17728-116">Remarks</span></span>

<span data-ttu-id="17728-117">Операции на объект, представленный этой **записи** могут завершиться с ошибкой после завершения этого метода.</span><span class="sxs-lookup"><span data-stu-id="17728-117">Operations on the object represented by this **Record** may fail after this method completes.</span></span> <span data-ttu-id="17728-118">После вызова **макрокоманду УдалитьЗапись** **записи** должны быть закрыты, так как поведение **записи** могут стать непредсказуемое в зависимости от, когда поставщик обновляет **запись** с источником данных.</span><span class="sxs-lookup"><span data-stu-id="17728-118">After calling **DeleteRecord**, the **Record** should be closed because the behavior of the **Record** may become unpredictable depending upon when the provider updates the **Record** with the data source.</span></span>

<span data-ttu-id="17728-119">Если эта **запись** был получен из [набора записей](recordset-object-ado.md), затем результаты этой операции будет не будут отражены сразу же в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="17728-119">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="17728-120">Обновление **набора записей** , закрыть и повторно открыть его или выполнив методы **записей** [запроса](requery-method-ado.md)или [обновления](update-method-ado.md) и [выполнить повторную синхронизацию](resync-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="17728-120">Refresh the **Recordset** by closing and re-opening it, or by executing the **Recordset** [Requery](requery-method-ado.md), or [Update](update-method-ado.md) and [Resync](resync-method-ado.md) methods.</span></span>


> [!NOTE]
> <span data-ttu-id="17728-121">URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="17728-121">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="17728-122">Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="17728-122">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


