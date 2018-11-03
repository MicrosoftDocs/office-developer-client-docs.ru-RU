---
title: Метод - Clear ActiveX Data Objects (ADO)
TOCTitle: Clear method (ADO)
ms:assetid: 5d51f42c-147b-1fcf-d05b-123e5714ecb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249329(v=office.15)
ms:contentKeyID: 48545110
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 459ce19fab15e3e9bbd886a0f063005dab674fbc
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929141"
---
# <a name="clear-method-ado"></a><span data-ttu-id="e5fce-102">Метод Clear (ADO)</span><span class="sxs-lookup"><span data-stu-id="e5fce-102">Clear method (ADO)</span></span>


<span data-ttu-id="e5fce-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5fce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e5fce-104">Удаляет все объекты **ошибок** из семейства **Errors** .</span><span class="sxs-lookup"><span data-stu-id="e5fce-104">Removes all the **Error** objects from the **Errors** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5fce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5fce-105">Syntax</span></span>

<span data-ttu-id="e5fce-106">*Ошибки*. Очистить</span><span class="sxs-lookup"><span data-stu-id="e5fce-106">*Errors*.Clear</span></span>

## <a name="remarks"></a><span data-ttu-id="e5fce-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5fce-107">Remarks</span></span>

<span data-ttu-id="e5fce-108">Используйте метод **Clear** на семейство [Errors](errors-collection-ado.md) для удаления всех существующих объектов [Error](error-object-ado.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="e5fce-108">Use the **Clear** method on the [Errors](errors-collection-ado.md) collection to remove all existing [Error](error-object-ado.md) objects from the collection.</span></span> <span data-ttu-id="e5fce-109">При возникновении ошибки ADO автоматически удаляет семейство **Errors** и заполняется **Ошибка** объекты, основанные на новой ошибки.</span><span class="sxs-lookup"><span data-stu-id="e5fce-109">When an error occurs, ADO automatically clears the **Errors** collection and fills it with **Error** objects based on the new error.</span></span>

<span data-ttu-id="e5fce-110">Некоторые свойства и методы возвращают предупреждения, которые отображаются в виде объектов **ошибок** в семействе **Errors** , но не приостановить выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="e5fce-110">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution.</span></span> <span data-ttu-id="e5fce-111">Прежде чем обращаться [выполнить повторную синхронизацию](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md)или [CancelBatch](cancelbatch-method-ado.md) методы объекта [набора записей](recordset-object-ado.md) ; метод [Open](open-method-ado-connection.md) объекта [подключения](connection-object-ado.md) ; или задать свойство [фильтра](filter-property-ado.md) для объекта **набора записей** , вызовите метод **Clear** на семейство **Errors** .</span><span class="sxs-lookup"><span data-stu-id="e5fce-111">Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object; the [Open](open-method-ado-connection.md) method on a [Connection](connection-object-ado.md) object; or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection.</span></span> <span data-ttu-id="e5fce-112">Таким образом, могут читать свойство [Count](count-property-ado.md) коллекции **ошибок** для проверки возвращенных предупреждения.</span><span class="sxs-lookup"><span data-stu-id="e5fce-112">That way, you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>

