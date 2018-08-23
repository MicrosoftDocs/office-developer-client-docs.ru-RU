---
title: Отображение свойств конфигурации
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fa48e97ed25fe1175ffd3a92ac961dcf5bde50b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588358"
---
# <a name="displaying-configuration-property-sheets"></a><span data-ttu-id="df40b-103">Отображение свойств конфигурации</span><span class="sxs-lookup"><span data-stu-id="df40b-103">Displaying configuration property sheets</span></span>

<span data-ttu-id="df40b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df40b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df40b-105">Поставщики транспорта используйте метод [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) для реализации свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="df40b-105">Transport providers use the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to implement configuration property sheets.</span></span> <span data-ttu-id="df40b-106">При вызове **DoConfigPropSheet**, поставщика транспорта передает в указатель массив свойств, а также сведения о том, как они отображаются.</span><span class="sxs-lookup"><span data-stu-id="df40b-106">When calling **DoConfigPropSheet**, the transport provider passes in a pointer to an array of properties along with information about how to display them.</span></span> <span data-ttu-id="df40b-107">MAPI затем представлены свойства для пользователя с помощью стандартного диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="df40b-107">MAPI then presents the properties to the user by means of a standard dialog box.</span></span> <span data-ttu-id="df40b-108">Вы являетесь настоятельно рекомендуется использовать этот механизм sheet свойства при реализации поставщика транспорта из-за преимущество пользователю согласованный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="df40b-108">You are strongly encouraged to use this property sheet mechanism when implementing your transport provider due to the benefit to the user of a consistent interface.</span></span>
  
## <a name="transport-providers"></a><span data-ttu-id="df40b-109">Поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="df40b-109">Transport providers</span></span>

<span data-ttu-id="df40b-110">Поставщики транспорта можно использовать функцию [BuildDisplayTable](builddisplaytable.md) для упрощения создания таблицы отображения для использования с **DoConfigPropSheet**.</span><span class="sxs-lookup"><span data-stu-id="df40b-110">Transport providers can use the [BuildDisplayTable](builddisplaytable.md) function to simplify construction of a display table for use with **DoConfigPropSheet**.</span></span> <span data-ttu-id="df40b-111">Поставщики транспорта также можно использовать API-интерфейса страницы свойств напрямую.</span><span class="sxs-lookup"><span data-stu-id="df40b-111">Transport providers can also use the property sheet API directly.</span></span> <span data-ttu-id="df40b-112">Для изменения свойств буферов, поставщиками транспорта можно использовать функцию [CreateIProp](createiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="df40b-112">To buffer changes to the properties, transport providers can use the [CreateIProp](createiprop.md) function.</span></span> <span data-ttu-id="df40b-113">Это упрощает обработка отмен пользователем, пока пользователь изменяет значения, хранящиеся в свойствах.</span><span class="sxs-lookup"><span data-stu-id="df40b-113">This simplifies the handling of cancellations by the user while the user modifies the values stored in the properties.</span></span> <span data-ttu-id="df40b-114">При необходимости, поставщика транспорта можно также задать диалоговое окно Мастер создания поля для упрощения задачи настройки для пользователя.</span><span class="sxs-lookup"><span data-stu-id="df40b-114">If necessary, a transport provider can also provide a wizard dialog box to simplify configuration tasks for the user.</span></span> 
  

