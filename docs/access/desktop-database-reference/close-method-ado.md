---
title: Метод - Close ActiveX Data Objects (ADO)
TOCTitle: Close Method (ADO)
ms:assetid: 26a7cced-ebeb-70be-f5de-96a35711bc37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249029(v=office.15)
ms:contentKeyID: 48543818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2df2f04f54242186093122bf70ef3365ad8617bf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875821"
---
# <a name="close-method-ado"></a><span data-ttu-id="a2936-102">Закройте метод (ADO)</span><span class="sxs-lookup"><span data-stu-id="a2936-102">Close Method (ADO)</span></span>


<span data-ttu-id="a2936-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2936-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a2936-104">Закрывает открытый объект и любые зависящие объекты.</span><span class="sxs-lookup"><span data-stu-id="a2936-104">Closes an open object and any dependent objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2936-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2936-105">Syntax</span></span>

<span data-ttu-id="a2936-106">*object*.Close</span><span class="sxs-lookup"><span data-stu-id="a2936-106">*object*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="a2936-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="a2936-107">Remarks</span></span>

<span data-ttu-id="a2936-108">Используйте метод **Close** для закрытия [подключения](connection-object-ado.md), [записи](record-object-ado.md), [набора записей](recordset-object-ado.md)или объект [Stream](stream-object-ado.md) , чтобы освободить место на все связанные системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="a2936-108">Use the **Close** method to close a [Connection](connection-object-ado.md), a [Record](record-object-ado.md), a [Recordset](recordset-object-ado.md), or a [Stream](stream-object-ado.md) object to free any associated system resources.</span></span> <span data-ttu-id="a2936-109">Закрытие объект не удаляется из памяти; можно изменить параметры его свойств и откройте его позже.</span><span class="sxs-lookup"><span data-stu-id="a2936-109">Closing an object does not remove it from memory; you can change its property settings and open it again later.</span></span> <span data-ttu-id="a2936-110">Чтобы полностью удалить объект из памяти, задайте объектной переменной значение *Nothing* (в Visual Basic) после закрытия объекта.</span><span class="sxs-lookup"><span data-stu-id="a2936-110">To completely eliminate an object from memory, set the object variable to *Nothing* (in Visual Basic) after closing the object.</span></span>

<span data-ttu-id="a2936-111">**Подключение**</span><span class="sxs-lookup"><span data-stu-id="a2936-111">**Connection**</span></span>

<span data-ttu-id="a2936-112">Также с помощью метода **Закрыть** , чтобы закрыть объект **подключения** закрывает любые active объекты **набора записей** , связанные с подключением.</span><span class="sxs-lookup"><span data-stu-id="a2936-112">Using the **Close** method to close a **Connection** object also closes any active **Recordset** objects associated with the connection.</span></span> <span data-ttu-id="a2936-113">Объект [команды](command-object-ado.md) , связанного с объектом **подключения** , закрытие будут сохранены и отобразятся, однако он больше не будет связан с объектом **подключения** ; то есть его свойство [ActiveConnection](activeconnection-property-ado.md) устанавливается значение **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="a2936-113">A [Command](command-object-ado.md) object associated with the **Connection** object you are closing will persist, but it will no longer be associated with a **Connection** object; that is, its [ActiveConnection](activeconnection-property-ado.md) property will be set to **Nothing**.</span></span> <span data-ttu-id="a2936-114">Кроме того коллекции [параметров](parameters-collection-ado.md) объекта **команды** будут удалены из параметров, определенных поставщиком.</span><span class="sxs-lookup"><span data-stu-id="a2936-114">Also, the **Command** object's [Parameters](parameters-collection-ado.md) collection will be cleared of any provider-defined parameters.</span></span>

<span data-ttu-id="a2936-115">Позднее можно вызвать метод [Open](open-method-ado-connection.md) , чтобы повторно установить подключение к тому же или другой источник данных.</span><span class="sxs-lookup"><span data-stu-id="a2936-115">You can later call the [Open](open-method-ado-connection.md) method to re-establish the connection to the same, or another, data source.</span></span> <span data-ttu-id="a2936-116">При закрытии объекта **подключения** вызов любых методов, которые требуют открытое подключение к источнику данных приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="a2936-116">While the **Connection** object is closed, calling any methods that require an open connection to the data source generates an error.</span></span>

<span data-ttu-id="a2936-117">Закрытие объект **подключения** при подключение open объектов **наборов записей** откат отложенные изменения из всех объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="a2936-117">Closing a **Connection** object while there are open **Recordset** objects on the connection rolls back any pending changes in all of the **Recordset** objects.</span></span> <span data-ttu-id="a2936-118">Явное закрытие объект **подключения** (вызов метода **Close** ) во время операции хода выполнения создает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a2936-118">Explicitly closing a **Connection** object (calling the **Close** method) while a transaction is in progress generates an error.</span></span> <span data-ttu-id="a2936-119">Если объект **подключения** выходит из области действия транзакции во время выполнения, ADO автоматически выполняет откат транзакции.</span><span class="sxs-lookup"><span data-stu-id="a2936-119">If a **Connection** object falls out of scope while a transaction is in progress, ADO automatically rolls back the transaction.</span></span>

<span data-ttu-id="a2936-120">**Набор записей, записи, в потоковом режиме**</span><span class="sxs-lookup"><span data-stu-id="a2936-120">**Recordset, Record, Stream**</span></span>

<span data-ttu-id="a2936-121">С помощью **Закрыть** метод закрытия объекта **набора записей**, **записи**или **поток** освобождает связанных данных и монопольном, которые вы могли данных через этот определенный объект.</span><span class="sxs-lookup"><span data-stu-id="a2936-121">Using the **Close** method to close a **Recordset**, **Record**, or **Stream** object releases the associated data and any exclusive access you may have had to the data through this particular object.</span></span> <span data-ttu-id="a2936-122">Позднее можно вызвать метод [Open](open-method-ado-recordset.md) и снова откройте объект с атрибутами же или измененные.</span><span class="sxs-lookup"><span data-stu-id="a2936-122">You can later call the [Open](open-method-ado-recordset.md) method to reopen the object with the same, or modified, attributes.</span></span>

<span data-ttu-id="a2936-123">При закрытии объекта **набора записей** вызов любых методов, которые требуют live текущей позиции приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="a2936-123">While a **Recordset** object is closed, calling any methods that require a live cursor generates an error.</span></span>

<span data-ttu-id="a2936-124">Если редактирование выполняется в режиме немедленное обновление, вызвав метод **Close** приводит к ошибке; Вместо этого вызовите метод [Update](update-method-ado.md) или [CancelUpdate](cancelupdate-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a2936-124">If an edit is in progress while in immediate update mode, calling the **Close** method generates an error; instead, call the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method first.</span></span> <span data-ttu-id="a2936-125">При закрытии объекта **набора записей** при в пакетном режиме обновление всех изменений с момента последнего вызова [UpdateBatch](updatebatch-method-ado.md) не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="a2936-125">If you close the **Recordset** object while in batch update mode, all changes since the last [UpdateBatch](updatebatch-method-ado.md) call are lost.</span></span>

<span data-ttu-id="a2936-126">При использовании метода [клонирования](clone-method-ado.md) создание копий open объекта **набора записей** закрытия исходной или клонирована не влияет на какие-либо других копий.</span><span class="sxs-lookup"><span data-stu-id="a2936-126">If you use the [Clone](clone-method-ado.md) method to create copies of an open **Recordset** object, closing the original or a clone does not affect any of the other copies.</span></span>

