---
title: Архитектура Outlook PIA
TOCTitle: Architecture of the Outlook PIA
ms:assetid: 89577d14-e6e2-4270-8e72-b0adba378667
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646255(v=office.15)
ms:contentKeyID: 55119777
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 37ecad42b08b96d79d96d62f98e27913a0309971
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336528"
---
# <a name="architecture-of-the-outlook-pia"></a><span data-ttu-id="22810-102">Архитектура Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="22810-102">Architecture of the Outlook PIA</span></span>

<span data-ttu-id="22810-103">Основная сборка взаимодействия Outlook (PIA) полностью поддерживает разработку управляемого кода с использованием объектной модели Outlook.</span><span class="sxs-lookup"><span data-stu-id="22810-103">The Outlook Primary Interop Assembly (PIA) fully supports developing against the Outlook object model in managed code.</span></span> <span data-ttu-id="22810-104">Но при первом взгляде на PIA в обозревателе объектов можно удивиться обилию лишних интерфейсов, содержащихся в PIA, и тому факту, что не все члены  методы, свойства и события  объекта представлены одним и тем же интерфейсом объекта.</span><span class="sxs-lookup"><span data-stu-id="22810-104">However, when you look at the PIA in an object browser for the first time, you may be surprised by the many extra interfaces that the PIA contains, and the fact that not all method, property, and event members of an object are exposed by the same object interface.</span></span> <span data-ttu-id="22810-105">Подразделы этого раздела содержат указания по доступу из кода к членам объектов, а также по поиску справки для объектов, методов, свойств и событий.</span><span class="sxs-lookup"><span data-stu-id="22810-105">The topics in this section describe guidelines for how to access object members in code, and where to look for help for objects, methods, properties, and events.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="22810-106">В этой статье</span><span class="sxs-lookup"><span data-stu-id="22810-106">In this section</span></span>

|<span data-ttu-id="22810-107">Статья</span><span class="sxs-lookup"><span data-stu-id="22810-107">Topic</span></span>|<span data-ttu-id="22810-108">Описание</span><span class="sxs-lookup"><span data-stu-id="22810-108">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="22810-109">Связывание Outlook PIA с объектной моделью</span><span class="sxs-lookup"><span data-stu-id="22810-109">Relating the Outlook PIA with the object model</span></span>](relating-the-outlook-pia-with-the-object-model.md) |<span data-ttu-id="22810-110">Описывает порядок сопоставления объектов и элементов объектной модели Outlook на основе COM соответствующим управляемым интерфейсам и классам PIA.</span><span class="sxs-lookup"><span data-stu-id="22810-110">Describes how objects and members in the COM-based Outlook object model are mapped to corresponding managed interfaces and classes in the PIA.</span></span>|
|[<span data-ttu-id="22810-111">Объекты в Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="22810-111">Objects in the Outlook PIA</span></span>](objects-in-the-outlook-pia.md) |<span data-ttu-id="22810-112">Описывает типовые интерфейсы, классы и делегаты .NET, сопоставляемые с COM-объектом, а также описывает доступ к объекту в PIA.</span><span class="sxs-lookup"><span data-stu-id="22810-112">Describes the typical .NET interfaces, classes, and delegates that are mapped to a COM object, and describes how to access an object in the PIA.</span></span>|
|[<span data-ttu-id="22810-113">Методы и свойства в Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="22810-113">Methods and properties in the Outlook PIA</span></span>](methods-and-properties-in-the-outlook-pia.md) |<span data-ttu-id="22810-114">Описывает, как получить доступ к методам и свойствам объекта в управляемом коде с помощью PIA.</span><span class="sxs-lookup"><span data-stu-id="22810-114">Describes how to access methods and properties of an object in managed code by using the PIA.</span></span>|
|[<span data-ttu-id="22810-115">События в Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="22810-115">Events in the Outlook PIA</span></span>](events-in-the-outlook-pia.md) |<span data-ttu-id="22810-116">Описывает интерфейсы, связанные с событиями, делегаты и классы модуля поддержки приемника в PIA.</span><span class="sxs-lookup"><span data-stu-id="22810-116">Describes event-related interfaces, delegates, and sink helper classes in the PIA.</span></span>|

## <a name="see-also"></a><span data-ttu-id="22810-117">См. также</span><span class="sxs-lookup"><span data-stu-id="22810-117">See also</span></span>

- [<span data-ttu-id="22810-118">Подготовка использования Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="22810-118">Setting up to use the Outlook PIA</span></span>](setting-up-to-use-the-outlook-pia.md)
- [<span data-ttu-id="22810-119">Разработка управляемых надстроек для Outlook с помощью Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="22810-119">Developing managed Outlook add-ins using the Outlook PIA</span></span>](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [<span data-ttu-id="22810-120">Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="22810-120">How do I... (Outlook 2013 PIA Reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

