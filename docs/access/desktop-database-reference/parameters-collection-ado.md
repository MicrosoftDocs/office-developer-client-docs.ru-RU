---
title: Коллекция Parameters (ADO)
TOCTitle: Parameters collection (ADO)
ms:assetid: 554387c3-3572-5391-3b24-c7d3443844cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249283(v=office.15)
ms:contentKeyID: 48544923
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231103
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: feb24e0f498e02bae01ef689a2ad62e487e314bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287946"
---
# <a name="parameters-collection-ado"></a><span data-ttu-id="cc20c-102">Коллекция Parameters (ADO)</span><span class="sxs-lookup"><span data-stu-id="cc20c-102">Parameters collection (ADO)</span></span>


<span data-ttu-id="cc20c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc20c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc20c-104">Содержит все [объекты Parameter](parameter-object-ado.md) объекта [Command.](command-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="cc20c-104">Contains all the [Parameter](parameter-object-ado.md) objects of a [Command](command-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc20c-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="cc20c-105">Remarks</span></span>

<span data-ttu-id="cc20c-106">Объект **Command** имеет коллекцию **Parameters,** которая состоит из **объектов Parameter.**</span><span class="sxs-lookup"><span data-stu-id="cc20c-106">A **Command** object has a **Parameters** collection made up of **Parameter** objects.</span></span>

<span data-ttu-id="cc20c-107">Использование метода [Refresh](refresh-method-ado.md) в коллекции **parameters** объекта **Command** извлекает сведения о параметрах поставщика для хранимой процедуры или параметризованного запроса, указанного в **объекте Command.**</span><span class="sxs-lookup"><span data-stu-id="cc20c-107">Using the [Refresh](refresh-method-ado.md) method on a **Command** object's **Parameters** collection retrieves provider parameter information for the stored procedure or parameterized query specified in the **Command** object.</span></span> <span data-ttu-id="cc20c-108">Некоторые поставщики не поддерживают хранимые вызовы процедур или параметризованные запросы; Вызов метода **Refresh** для коллекции **Parameters** при использовании такого поставщика возвратит ошибку.</span><span class="sxs-lookup"><span data-stu-id="cc20c-108">Some providers do not support stored procedure calls or parameterized queries; calling the **Refresh** method on the **Parameters** collection when using such a provider will return an error.</span></span>

<span data-ttu-id="cc20c-109">Если вы не определили собственные объекты **Parameter** и получили доступ к коллекции **Parameters** перед вызовом метода **Refresh,** ADO автоматически вызывает метод и заполняет коллекцию автоматически.</span><span class="sxs-lookup"><span data-stu-id="cc20c-109">If you have not defined your own **Parameter** objects and you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>

<span data-ttu-id="cc20c-110">Вы можете свести к минимуму вызовы поставщика для повышения производительности, если вы знаете свойства параметров, связанных с хранимой процедурой или параметризованный запрос, который требуется вызвать.</span><span class="sxs-lookup"><span data-stu-id="cc20c-110">You can minimize calls to the provider to improve performance if you know the properties of the parameters associated with the stored procedure or parameterized query you wish to call.</span></span> <span data-ttu-id="cc20c-111">Используйте метод [CreateParameter](createparameter-method-ado.md) для создания объектов **Parameter** с соответствующими параметрами свойств и с помощью метода [Append](append-method-ado.md) добавьте их в коллекцию **Parameters.**</span><span class="sxs-lookup"><span data-stu-id="cc20c-111">Use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the [Append](append-method-ado.md) method to add them to the **Parameters** collection.</span></span> <span data-ttu-id="cc20c-112">Это позволяет устанавливать и возвращать значения параметров без вызова поставщика для сведений о параметре.</span><span class="sxs-lookup"><span data-stu-id="cc20c-112">This lets you set and return parameter values without having to call the provider for the parameter information.</span></span> <span data-ttu-id="cc20c-113">Если вы пишете поставщику, который не передает сведения о параметрах, необходимо вручную заполнить коллекцию **параметров** с помощью этого метода, чтобы иметь возможность использовать параметры вообще.</span><span class="sxs-lookup"><span data-stu-id="cc20c-113">If you are writing to a provider that does not supply parameter information, you must manually populate the **Parameters** collection using this method to be able to use parameters at all.</span></span> <span data-ttu-id="cc20c-114">Используйте метод [Delete,](delete-method-ado-parameters-collection.md) чтобы при необходимости удалить **объекты Parameter** из коллекции **Parameters.**</span><span class="sxs-lookup"><span data-stu-id="cc20c-114">Use the [Delete](delete-method-ado-parameters-collection.md) method to remove **Parameter** objects from the **Parameters** collection if necessary.</span></span>

<span data-ttu-id="cc20c-115">Объекты в коллекции **Parameters** объекта **Recordset** выходить за пределы области (поэтому становятся недоступными) при закрытии **объекта Recordset.**</span><span class="sxs-lookup"><span data-stu-id="cc20c-115">The objects in the **Parameters** collection of a **Recordset** go out of scope (therefore becoming unavailable) when the **Recordset** is closed.</span></span>

