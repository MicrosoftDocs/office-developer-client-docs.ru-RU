---
title: Description Property (ADO)
TOCTitle: Description Property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3837d60b58772bbe6b65af6673c4eaa471507e66
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480538"
---
# <a name="description-property-ado"></a><span data-ttu-id="4ae08-102">Description Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="4ae08-102">Description Property (ADO)</span></span>


<span data-ttu-id="4ae08-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ae08-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4ae08-104">Описывает объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="4ae08-104">Describes an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ae08-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ae08-105">Return Value</span></span>

<span data-ttu-id="4ae08-106">Возвращает значение типа **String** , содержащее описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="4ae08-106">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ae08-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="4ae08-107">Remarks</span></span>

<span data-ttu-id="4ae08-108">Используйте свойство **Description** для получения краткое описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="4ae08-108">Use the **Description** property to obtain a short description of the error.</span></span> <span data-ttu-id="4ae08-109">Отображение этого свойства для оповещения пользователя об ошибке, не могут и не хотите обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="4ae08-109">Display this property to alert the user to an error that you cannot or do not want to handle.</span></span> <span data-ttu-id="4ae08-110">Строка будет получен из ADO или поставщика.</span><span class="sxs-lookup"><span data-stu-id="4ae08-110">The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="4ae08-111">Поставщики отвечают за передачей текст определенное сообщение об ошибке в ADO.</span><span class="sxs-lookup"><span data-stu-id="4ae08-111">Providers are responsible for passing specific error text to ADO.</span></span> <span data-ttu-id="4ae08-112">Добавляет объект [Error](error-object-ado.md) ADO коллекцию **ошибок** для каждого поставщика получает сообщение об ошибке или предупреждение его.</span><span class="sxs-lookup"><span data-stu-id="4ae08-112">ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives.</span></span> <span data-ttu-id="4ae08-113">Перечисление коллекции **ошибки** для ошибки, которые передает поставщика трассировки.</span><span class="sxs-lookup"><span data-stu-id="4ae08-113">Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>

