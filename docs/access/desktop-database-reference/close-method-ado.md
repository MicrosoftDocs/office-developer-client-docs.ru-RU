---
title: Close Method — ActiveX объектов данных (ADO)
TOCTitle: Close method (ADO)
ms:assetid: 26a7cced-ebeb-70be-f5de-96a35711bc37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249029(v=office.15)
ms:contentKeyID: 48543818
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 269a782e85fab1e5dc47cd32f2e2c11306e11470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296313"
---
# <a name="close-method-ado"></a><span data-ttu-id="bf82f-102">Метод Close (ADO)</span><span class="sxs-lookup"><span data-stu-id="bf82f-102">Close method (ADO)</span></span>


<span data-ttu-id="bf82f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf82f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bf82f-104">Закрывает открытый объект и все зависимые объекты.</span><span class="sxs-lookup"><span data-stu-id="bf82f-104">Closes an open object and any dependent objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf82f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf82f-105">Syntax</span></span>

<span data-ttu-id="bf82f-106">*object*.Close</span><span class="sxs-lookup"><span data-stu-id="bf82f-106">*object*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="bf82f-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf82f-107">Remarks</span></span>

<span data-ttu-id="bf82f-108">Используйте метод **Close,** чтобы закрыть [подключение,](connection-object-ado.md) [запись,](record-object-ado.md)набор записей [или](recordset-object-ado.md)объект [Stream,](stream-object-ado.md) чтобы освободить все связанные ресурсы системы.</span><span class="sxs-lookup"><span data-stu-id="bf82f-108">Use the **Close** method to close a [Connection](connection-object-ado.md), a [Record](record-object-ado.md), a [Recordset](recordset-object-ado.md), or a [Stream](stream-object-ado.md) object to free any associated system resources.</span></span> <span data-ttu-id="bf82f-109">Закрытие объекта не удаляет его из памяти; Вы можете изменить его параметры свойств и открыть его позже.</span><span class="sxs-lookup"><span data-stu-id="bf82f-109">Closing an object does not remove it from memory; you can change its property settings and open it again later.</span></span> <span data-ttu-id="bf82f-110">Чтобы полностью исключить объект из памяти, установите переменную объекта *Nothing* (Visual Basic) после закрытия объекта.</span><span class="sxs-lookup"><span data-stu-id="bf82f-110">To completely eliminate an object from memory, set the object variable to *Nothing* (in Visual Basic) after closing the object.</span></span>

<span data-ttu-id="bf82f-111">**Connection**</span><span class="sxs-lookup"><span data-stu-id="bf82f-111">**Connection**</span></span>

<span data-ttu-id="bf82f-112">С помощью **метода Close** для закрытия объекта **Подключения** также закрываются все активные объекты **Recordset,** связанные с подключением.</span><span class="sxs-lookup"><span data-stu-id="bf82f-112">Using the **Close** method to close a **Connection** object also closes any active **Recordset** objects associated with the connection.</span></span> <span data-ttu-id="bf82f-113">Объект [Command,](command-object-ado.md) связанный с закрываемом объектом **Подключения,** будет сохраняться, но он больше не будет связан с объектом **Подключения;** то есть свойство [ActiveConnection](activeconnection-property-ado.md) будет настроено на **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="bf82f-113">A [Command](command-object-ado.md) object associated with the **Connection** object you are closing will persist, but it will no longer be associated with a **Connection** object; that is, its [ActiveConnection](activeconnection-property-ado.md) property will be set to **Nothing**.</span></span> <span data-ttu-id="bf82f-114">Кроме того, **коллекция** параметров объекта [Command](parameters-collection-ado.md) будет очищена от параметров, определенных поставщиком.</span><span class="sxs-lookup"><span data-stu-id="bf82f-114">Also, the **Command** object's [Parameters](parameters-collection-ado.md) collection will be cleared of any provider-defined parameters.</span></span>

<span data-ttu-id="bf82f-115">Позже можно вызвать метод [Open,](open-method-ado-connection.md) чтобы восстановить подключение к одному или другому источнику данных.</span><span class="sxs-lookup"><span data-stu-id="bf82f-115">You can later call the [Open](open-method-ado-connection.md) method to re-establish the connection to the same, or another, data source.</span></span> <span data-ttu-id="bf82f-116">В то время как объект **Connection** закрыт, вызов любых методов, которые требуют открытого подключения к источнику данных, создает ошибку.</span><span class="sxs-lookup"><span data-stu-id="bf82f-116">While the **Connection** object is closed, calling any methods that require an open connection to the data source generates an error.</span></span>

<span data-ttu-id="bf82f-117">Закрытие объекта **Подключения** при открытых объектах **Recordset** в подключении откатит все ожидающих изменений во всех объектах **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="bf82f-117">Closing a **Connection** object while there are open **Recordset** objects on the connection rolls back any pending changes in all of the **Recordset** objects.</span></span> <span data-ttu-id="bf82f-118">Явное закрытие объекта **Подключения** (вызов метода **Закрыть)** во время выполнения транзакции создает ошибку.</span><span class="sxs-lookup"><span data-stu-id="bf82f-118">Explicitly closing a **Connection** object (calling the **Close** method) while a transaction is in progress generates an error.</span></span> <span data-ttu-id="bf82f-119">Если объект **Connection** выходит из сферы действия во время выполнения транзакции, ADO автоматически откатает транзакцию.</span><span class="sxs-lookup"><span data-stu-id="bf82f-119">If a **Connection** object falls out of scope while a transaction is in progress, ADO automatically rolls back the transaction.</span></span>

<span data-ttu-id="bf82f-120">**Recordset, Record, Stream**</span><span class="sxs-lookup"><span data-stu-id="bf82f-120">**Recordset, Record, Stream**</span></span>

<span data-ttu-id="bf82f-121">С помощью **метода Close** для закрытия объекта **Recordset,** **Record** или **Stream** высвобовывающие связанные данные и любой эксклюзивный доступ к данным через этот объект.</span><span class="sxs-lookup"><span data-stu-id="bf82f-121">Using the **Close** method to close a **Recordset**, **Record**, or **Stream** object releases the associated data and any exclusive access you may have had to the data through this particular object.</span></span> <span data-ttu-id="bf82f-122">Позже можно вызвать метод [Open](open-method-ado-recordset.md) для повторного открытия объекта с помощью тех же или измененных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="bf82f-122">You can later call the [Open](open-method-ado-recordset.md) method to reopen the object with the same, or modified, attributes.</span></span>

<span data-ttu-id="bf82f-123">В то время как объект **Recordset** закрыт, вызов любых методов, которые требуют живого курсора, создает ошибку.</span><span class="sxs-lookup"><span data-stu-id="bf82f-123">While a **Recordset** object is closed, calling any methods that require a live cursor generates an error.</span></span>

<span data-ttu-id="bf82f-124">Если изменение продолжается в режиме немедленного обновления, вызов метода **Close** создает ошибку; вместо этого сначала [позвоните методу Update](update-method-ado.md) или [CancelUpdate.](cancelupdate-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="bf82f-124">If an edit is in progress while in immediate update mode, calling the **Close** method generates an error; instead, call the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method first.</span></span> <span data-ttu-id="bf82f-125">Если закрыть объект **Recordset** в режиме пакетного обновления, все изменения после последнего вызова [UpdateBatch](updatebatch-method-ado.md) будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="bf82f-125">If you close the **Recordset** object while in batch update mode, all changes since the last [UpdateBatch](updatebatch-method-ado.md) call are lost.</span></span>

<span data-ttu-id="bf82f-126">Если метод [клона](clone-method-ado.md) используется для создания копий открытого объекта **Recordset,** закрытие исходного или клона не влияет ни на один из других экземпляров.</span><span class="sxs-lookup"><span data-stu-id="bf82f-126">If you use the [Clone](clone-method-ado.md) method to create copies of an open **Recordset** object, closing the original or a clone does not affect any of the other copies.</span></span>

