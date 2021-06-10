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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293996"
---
# <a name="deleterecord-method-ado"></a><span data-ttu-id="f3dc0-102">Метод DeleteRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="f3dc0-102">DeleteRecord method (ADO)</span></span>

<span data-ttu-id="f3dc0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3dc0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f3dc0-104">Удаляет объект, представленный [записью.](record-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="f3dc0-104">Deletes a the entity represented by a [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3dc0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3dc0-105">Syntax</span></span>

<span data-ttu-id="f3dc0-106">*Запись*.\**DeleteRecord\*\*\*Source*, *Async*</span><span class="sxs-lookup"><span data-stu-id="f3dc0-106">*Record*.\**DeleteRecord\*\*\*Source*, *Async*</span></span>

## <a name="parameters"></a><span data-ttu-id="f3dc0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3dc0-107">Parameters</span></span>

|<span data-ttu-id="f3dc0-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="f3dc0-108">Parameter</span></span>|<span data-ttu-id="f3dc0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f3dc0-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f3dc0-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="f3dc0-110">*Source*</span></span> |<span data-ttu-id="f3dc0-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="f3dc0-111">Optional.</span></span> <span data-ttu-id="f3dc0-112">Значение **String,** содержаее URL-адрес, определяющий объект (например, файл или каталог), который будет удален.</span><span class="sxs-lookup"><span data-stu-id="f3dc0-112">A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted.</span></span> <span data-ttu-id="f3dc0-113">Если *Source* опущен или указывает пустую строку, объект, представленный текущей [записью,](record-object-ado.md) удаляется.</span><span class="sxs-lookup"><span data-stu-id="f3dc0-113">If *Source* is omitted or specifies an empty string, the entity represented by the current [Record](record-object-ado.md) is deleted.</span></span> <span data-ttu-id="f3dc0-114">Если запись — это запись коллекции [(RecordType](recordtype-property-ado.md) **adCollectionRecord**, например каталог), все дети (например, поднаправления) также будут удалены.</span><span class="sxs-lookup"><span data-stu-id="f3dc0-114">If the Record is a collection record ([RecordType](recordtype-property-ado.md) of **adCollectionRecord**, such as a directory) all children (for example, subdirectories) will also be deleted.</span></span>|
|<span data-ttu-id="f3dc0-115">*Async*</span><span class="sxs-lookup"><span data-stu-id="f3dc0-115">*Async*</span></span> |<span data-ttu-id="f3dc0-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="f3dc0-116">Optional.</span></span> <span data-ttu-id="f3dc0-117">Значение **Boolean,** которое при **True** указывает, что операция удаления асинхронна.</span><span class="sxs-lookup"><span data-stu-id="f3dc0-117">A **Boolean** value that, when **True**, specifies that the delete operation is asynchronous.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f3dc0-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="f3dc0-118">Remarks</span></span>

<span data-ttu-id="f3dc0-119">Операции на объекте, представленного этой **записью,** могут завершиться сбой после завершения этого метода.</span><span class="sxs-lookup"><span data-stu-id="f3dc0-119">Operations on the object represented by this **Record** may fail after this method completes.</span></span> <span data-ttu-id="f3dc0-120">После вызова **DeleteRecord** запись должна быть закрыта, так как поведение записи может стать  непредсказуемым в зависимости от того, когда поставщик обновляет запись с источником данных.  </span><span class="sxs-lookup"><span data-stu-id="f3dc0-120">After calling **DeleteRecord**, the **Record** should be closed because the behavior of the **Record** may become unpredictable depending upon when the provider updates the **Record** with the data source.</span></span>

<span data-ttu-id="f3dc0-121">Если эта **запись** была получена из [recordset,](recordset-object-ado.md)результаты этой операции не будут немедленно отражены в **Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="f3dc0-121">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="f3dc0-122">**Обновите набор записей,** закрыв и открыв его повторно или исполнив методы [Requery](requery-method-ado.md) **Recordset** или [Update](update-method-ado.md) и [Resync.](resync-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="f3dc0-122">Refresh the **Recordset** by closing and re-opening it, or by executing the **Recordset** [Requery](requery-method-ado.md), or [Update](update-method-ado.md) and [Resync](resync-method-ado.md) methods.</span></span>

> [!NOTE]
> <span data-ttu-id="f3dc0-123">URL-адреса, использующие схему http, автоматически вызывают поставщика DB Microsoft [OLE для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md)</span><span class="sxs-lookup"><span data-stu-id="f3dc0-123">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="f3dc0-124">Дополнительные сведения см. в [url-адресах Absolute и relative.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="f3dc0-124">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


