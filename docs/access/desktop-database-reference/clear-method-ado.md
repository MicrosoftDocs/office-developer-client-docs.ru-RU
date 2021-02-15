---
title: Метод Clear — ActiveX Data Objects (ADO)
TOCTitle: Clear method (ADO)
ms:assetid: 5d51f42c-147b-1fcf-d05b-123e5714ecb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249329(v=office.15)
ms:contentKeyID: 48545110
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b0d76480bdb5d5a3ab258e103a00707af303a4d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296362"
---
# <a name="clear-method-ado"></a><span data-ttu-id="69744-102">Метод Clear (ADO)</span><span class="sxs-lookup"><span data-stu-id="69744-102">Clear method (ADO)</span></span>


<span data-ttu-id="69744-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69744-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69744-104">Удаляет все объекты **Error** из коллекции **Errors.**</span><span class="sxs-lookup"><span data-stu-id="69744-104">Removes all the **Error** objects from the **Errors** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="69744-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69744-105">Syntax</span></span>

<span data-ttu-id="69744-106">*Ошибки.* Очистить</span><span class="sxs-lookup"><span data-stu-id="69744-106">*Errors*.Clear</span></span>

## <a name="remarks"></a><span data-ttu-id="69744-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="69744-107">Remarks</span></span>

<span data-ttu-id="69744-108">Используйте метод **Clear** для коллекции [Errors,](errors-collection-ado.md) чтобы удалить все существующие объекты [Error](error-object-ado.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="69744-108">Use the **Clear** method on the [Errors](errors-collection-ado.md) collection to remove all existing [Error](error-object-ado.md) objects from the collection.</span></span> <span data-ttu-id="69744-109">При ошибке ADO автоматически очищает коллекцию **Errors** и заполняет ее объектами **Error** в зависимости от новой ошибки.</span><span class="sxs-lookup"><span data-stu-id="69744-109">When an error occurs, ADO automatically clears the **Errors** collection and fills it with **Error** objects based on the new error.</span></span>

<span data-ttu-id="69744-110">Некоторые свойства и методы возвращают предупреждения, которые отображаются как объекты **Error** в коллекции **Errors,** но не останавливают выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="69744-110">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution.</span></span> <span data-ttu-id="69744-111">Перед вызовом [методов Resync,](resync-method-ado.md) [UpdateBatch](updatebatch-method-ado.md)или [CancelBatch](cancelbatch-method-ado.md) для объекта [Recordset;](recordset-object-ado.md) Метод [Open](open-method-ado-connection.md) для объекта [Connection;](connection-object-ado.md) или установите свойство [Filter](filter-property-ado.md) для объекта **Recordset,** вызовите метод **Clear** в коллекции **Errors.**</span><span class="sxs-lookup"><span data-stu-id="69744-111">Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object; the [Open](open-method-ado-connection.md) method on a [Connection](connection-object-ado.md) object; or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection.</span></span> <span data-ttu-id="69744-112">Таким образом можно считать свойство [Count](count-property-ado.md) коллекции **Errors** для проверки на возвращенных предупреждений.</span><span class="sxs-lookup"><span data-stu-id="69744-112">That way, you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>

