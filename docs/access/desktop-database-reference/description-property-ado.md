---
title: Свойство Description (ADO)
TOCTitle: Description property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba6d05aa1bfb626520af60a30279983bae6fa566
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293933"
---
# <a name="description-property-ado"></a><span data-ttu-id="d2eb2-102">Свойство Description (ADO)</span><span class="sxs-lookup"><span data-stu-id="d2eb2-102">Description property (ADO)</span></span>


<span data-ttu-id="d2eb2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2eb2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2eb2-104">Описывает объект [Error.](error-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d2eb2-104">Describes an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="d2eb2-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2eb2-105">Return value</span></span>

<span data-ttu-id="d2eb2-106">Возвращает значение **String,** содержаное описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="d2eb2-106">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2eb2-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="d2eb2-107">Remarks</span></span>

<span data-ttu-id="d2eb2-108">Чтобы **получить** краткое описание ошибки, используйте свойство Description.</span><span class="sxs-lookup"><span data-stu-id="d2eb2-108">Use the **Description** property to obtain a short description of the error.</span></span> <span data-ttu-id="d2eb2-109">Отобразить это свойство, чтобы предупредить пользователя об ошибке, которую невозможно или не нужно обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="d2eb2-109">Display this property to alert the user to an error that you cannot or do not want to handle.</span></span> <span data-ttu-id="d2eb2-110">Строка будет приходить либо от ADO, либо от поставщика.</span><span class="sxs-lookup"><span data-stu-id="d2eb2-110">The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="d2eb2-111">Поставщики несут ответственность за передачу определенного текста ошибки в ADO.</span><span class="sxs-lookup"><span data-stu-id="d2eb2-111">Providers are responsible for passing specific error text to ADO.</span></span> <span data-ttu-id="d2eb2-112">ADO добавляет объект [Ошибки](error-object-ado.md) в коллекцию **Ошибок** для каждого поставщика ошибки или предупреждения, которые он получает.</span><span class="sxs-lookup"><span data-stu-id="d2eb2-112">ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives.</span></span> <span data-ttu-id="d2eb2-113">Перенацелите коллекцию **ошибок,** чтобы отслеживать ошибки, которые передает поставщик.</span><span class="sxs-lookup"><span data-stu-id="d2eb2-113">Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>

