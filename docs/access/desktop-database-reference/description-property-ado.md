---
title: Свойство Description (ADO)
TOCTitle: Description property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc2a7706afbf69d9949e8b04122b144c6826ec40
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882940"
---
# <a name="description-property-ado"></a><span data-ttu-id="84004-102">Свойство Description (ADO)</span><span class="sxs-lookup"><span data-stu-id="84004-102">Description property (ADO)</span></span>


<span data-ttu-id="84004-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="84004-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="84004-104">Описывает объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="84004-104">Describes an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="84004-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84004-105">Return value</span></span>

<span data-ttu-id="84004-106">Возвращает значение типа **String** , содержащее описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="84004-106">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="84004-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="84004-107">Remarks</span></span>

<span data-ttu-id="84004-108">Используйте свойство **Description** для получения краткое описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="84004-108">Use the **Description** property to obtain a short description of the error.</span></span> <span data-ttu-id="84004-109">Отображение этого свойства для оповещения пользователя об ошибке, не могут и не хотите обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="84004-109">Display this property to alert the user to an error that you cannot or do not want to handle.</span></span> <span data-ttu-id="84004-110">Строка будет получен из ADO или поставщика.</span><span class="sxs-lookup"><span data-stu-id="84004-110">The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="84004-111">Поставщики отвечают за передачей текст определенное сообщение об ошибке в ADO.</span><span class="sxs-lookup"><span data-stu-id="84004-111">Providers are responsible for passing specific error text to ADO.</span></span> <span data-ttu-id="84004-112">Добавляет объект [Error](error-object-ado.md) ADO коллекцию **ошибок** для каждого поставщика получает сообщение об ошибке или предупреждение его.</span><span class="sxs-lookup"><span data-stu-id="84004-112">ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives.</span></span> <span data-ttu-id="84004-113">Перечисление коллекции **ошибки** для ошибки, которые передает поставщика трассировки.</span><span class="sxs-lookup"><span data-stu-id="84004-113">Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>

