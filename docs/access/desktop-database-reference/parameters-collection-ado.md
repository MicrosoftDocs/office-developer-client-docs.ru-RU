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
ms.openlocfilehash: 3a838819b2bac097d3f2fb704ef42c9d2329e51c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929904"
---
# <a name="parameters-collection-ado"></a><span data-ttu-id="c085c-102">Коллекция Parameters (ADO)</span><span class="sxs-lookup"><span data-stu-id="c085c-102">Parameters collection (ADO)</span></span>


<span data-ttu-id="c085c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c085c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c085c-104">Содержит все объекты [параметров](parameter-object-ado.md) объекта [Command](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c085c-104">Contains all the [Parameter](parameter-object-ado.md) objects of a [Command](command-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c085c-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="c085c-105">Remarks</span></span>

<span data-ttu-id="c085c-106">Объект **команды** имеет коллекцию **параметров** , состоящих из объектов **параметров** .</span><span class="sxs-lookup"><span data-stu-id="c085c-106">A **Command** object has a **Parameters** collection made up of **Parameter** objects.</span></span>

<span data-ttu-id="c085c-107">С помощью метода [обновления](refresh-method-ado.md) на коллекцию **параметров** объекта **команда** получает сведения о параметрах поставщика для хранимой процедуры или параметризованный запрос, указанный в объекте **команды** .</span><span class="sxs-lookup"><span data-stu-id="c085c-107">Using the [Refresh](refresh-method-ado.md) method on a **Command** object's **Parameters** collection retrieves provider parameter information for the stored procedure or parameterized query specified in the **Command** object.</span></span> <span data-ttu-id="c085c-108">Некоторые поставщики не поддерживают вызовы хранимых процедур или параметризованные запросы; вызов метода **обновления** на коллекцию **параметров** , при использовании такой поставщик возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c085c-108">Some providers do not support stored procedure calls or parameterized queries; calling the **Refresh** method on the **Parameters** collection when using such a provider will return an error.</span></span>

<span data-ttu-id="c085c-109">Если не определен **параметр** объектов и доступа к коллекции **параметров** , прежде чем вызывать метод **Refresh** , ADO автоматически вызовите метод и заполнения в коллекции.</span><span class="sxs-lookup"><span data-stu-id="c085c-109">If you have not defined your own **Parameter** objects and you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>

<span data-ttu-id="c085c-110">Можно свести к минимуму вызовы к поставщику для повышения производительности, если вы знаете свойств параметров, связанных с хранимую процедуру или параметризованный запрос, которые требуется позвонить.</span><span class="sxs-lookup"><span data-stu-id="c085c-110">You can minimize calls to the provider to improve performance if you know the properties of the parameters associated with the stored procedure or parameterized query you wish to call.</span></span> <span data-ttu-id="c085c-111">Метод [CreateParameter](createparameter-method-ado.md) используется для создания объектов **параметров** с соответствующими параметрами свойств и метод [Append](append-method-ado.md) используется для добавления их в коллекцию **параметров** .</span><span class="sxs-lookup"><span data-stu-id="c085c-111">Use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the [Append](append-method-ado.md) method to add them to the **Parameters** collection.</span></span> <span data-ttu-id="c085c-112">Это позволяет задать и возвращаемые значения параметра без вызова поставщика для получения параметров.</span><span class="sxs-lookup"><span data-stu-id="c085c-112">This lets you set and return parameter values without having to call the provider for the parameter information.</span></span> <span data-ttu-id="c085c-113">При создании поставщика, который не предоставляет сведений о параметрах необходимо вручную заполнить коллекцию **параметров** , с помощью этого метода должны иметь возможность использовать параметры вообще.</span><span class="sxs-lookup"><span data-stu-id="c085c-113">If you are writing to a provider that does not supply parameter information, you must manually populate the **Parameters** collection using this method to be able to use parameters at all.</span></span> <span data-ttu-id="c085c-114">Используйте метод [Delete](delete-method-ado-parameters-collection.md) для удаления **параметра** объектов из коллекции **параметров** при необходимости.</span><span class="sxs-lookup"><span data-stu-id="c085c-114">Use the [Delete](delete-method-ado-parameters-collection.md) method to remove **Parameter** objects from the **Parameters** collection if necessary.</span></span>

<span data-ttu-id="c085c-115">Объекты в коллекции **параметров** набора **записей** выйдет из области действия (таким образом недоступности) при закрытии **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="c085c-115">The objects in the **Parameters** collection of a **Recordset** go out of scope (therefore becoming unavailable) when the **Recordset** is closed.</span></span>

