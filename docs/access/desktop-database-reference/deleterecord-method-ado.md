---
title: DeleteRecord Method (ADO)
TOCTitle: DeleteRecord Method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d850234faf18a2bd6f3278ee4feade3aa3bb561
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479953"
---
# <a name="deleterecord-method-ado"></a><span data-ttu-id="bd3cb-102">DeleteRecord Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="bd3cb-102">DeleteRecord Method (ADO)</span></span>


<span data-ttu-id="bd3cb-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd3cb-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="bd3cb-104">Удаляет сущности, представленной в [записи](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="bd3cb-104">Deletes a the entity represented by a [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd3cb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd3cb-105">Syntax</span></span>

<span data-ttu-id="bd3cb-106">*Запись*. \**макрокоманду УдалитьЗапись \*\*\* источника*, *Async*</span><span class="sxs-lookup"><span data-stu-id="bd3cb-106">*Record*.\**DeleteRecord\*\*\*Source*, *Async*</span></span>

## <a name="parameters"></a><span data-ttu-id="bd3cb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd3cb-107">Parameters</span></span>

  - <span data-ttu-id="bd3cb-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="bd3cb-108">*Source*</span></span>

  - <span data-ttu-id="bd3cb-109">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-109">Optional.</span></span> <span data-ttu-id="bd3cb-110">**Строковое** значение, содержащее URL-адрес определение сущности (например, файл или каталог) для удаления.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-110">A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted.</span></span> <span data-ttu-id="bd3cb-111">Если *источник* указан или указывает пустая строка, удаляется сущности, представленной текущей [записи](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bd3cb-111">If *Source* is omitted or specifies an empty string, the entity represented by the current [Record](record-object-ado.md) is deleted.</span></span> <span data-ttu-id="bd3cb-112">Если запись является записью семейства сайтов ([типом записи](recordtype-property-ado.md) из **adCollectionRecord**, такие как каталог) также будут удалены все дочерние элементы (например, вложенные папки).</span><span class="sxs-lookup"><span data-stu-id="bd3cb-112">If the Record is a collection record ([RecordType](recordtype-property-ado.md) of **adCollectionRecord**, such as a directory) all children (for example, subdirectories) will also be deleted.</span></span>

  - <span data-ttu-id="bd3cb-113">*Async*</span><span class="sxs-lookup"><span data-stu-id="bd3cb-113">*Async*</span></span>

  - <span data-ttu-id="bd3cb-114">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-114">Optional.</span></span> <span data-ttu-id="bd3cb-115">**Логическое** значение, которое, если **значение True**, указывает, что асинхронной операции удаления.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-115">A **Boolean** value that, when **True**, specifies that the delete operation is asynchronous.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd3cb-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="bd3cb-116">Remarks</span></span>

<span data-ttu-id="bd3cb-117">Операции на объект, представленный этой **записи** могут завершиться с ошибкой после завершения этого метода.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-117">Operations on the object represented by this **Record** may fail after this method completes.</span></span> <span data-ttu-id="bd3cb-118">После вызова **макрокоманду УдалитьЗапись** **записи** должны быть закрыты, так как поведение **записи** могут стать непредсказуемое в зависимости от, когда поставщик обновляет **запись** с источником данных.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-118">After calling **DeleteRecord**, the **Record** should be closed because the behavior of the **Record** may become unpredictable depending upon when the provider updates the **Record** with the data source.</span></span>

<span data-ttu-id="bd3cb-119">Если эта **запись** был получен из [набора записей](recordset-object-ado.md), затем результаты этой операции будет не будут отражены сразу же в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-119">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="bd3cb-120">Обновление **набора записей** , закрыть и повторно открыть его или выполнив методы **записей** [запроса](requery-method-ado.md)или [обновления](update-method-ado.md) и [выполнить повторную синхронизацию](resync-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bd3cb-120">Refresh the **Recordset** by closing and re-opening it, or by executing the **Recordset** [Requery](requery-method-ado.md), or [Update](update-method-ado.md) and [Resync](resync-method-ado.md) methods.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bd3cb-121">URL-адреса, с помощью схемы http автоматически вызывает <A href="microsoft-ole-db-provider-for-internet-publishing.md">Поставщик Microsoft OLE DB для публикации Интернет</A>.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-121">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>.</span></span> <span data-ttu-id="bd3cb-122">Для получения дополнительных сведений см <A href="absolute-and-relative-urls.md">абсолютного и относительных URL-адресов</A>.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-122">For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


