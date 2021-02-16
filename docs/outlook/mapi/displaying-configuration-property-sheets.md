---
title: Отображение страниц свойств конфигурации
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a796f458e9d30206dc4c6feb37cbdb1e6b6a704b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421314"
---
# <a name="displaying-configuration-property-sheets"></a><span data-ttu-id="631a8-103">Отображение страниц свойств конфигурации</span><span class="sxs-lookup"><span data-stu-id="631a8-103">Displaying configuration property sheets</span></span>

<span data-ttu-id="631a8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="631a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="631a8-105">Поставщики транспорта используют метод [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) для реализации таблиц свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="631a8-105">Transport providers use the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to implement configuration property sheets.</span></span> <span data-ttu-id="631a8-106">При **вызове DoConfigPropSheet** поставщик транспорта передает указатель на массив свойств вместе с информацией о том, как их отображать.</span><span class="sxs-lookup"><span data-stu-id="631a8-106">When calling **DoConfigPropSheet**, the transport provider passes in a pointer to an array of properties along with information about how to display them.</span></span> <span data-ttu-id="631a8-107">Затем MAPI представляет свойства пользователю с помощью стандартного диалоговых окна.</span><span class="sxs-lookup"><span data-stu-id="631a8-107">MAPI then presents the properties to the user by means of a standard dialog box.</span></span> <span data-ttu-id="631a8-108">Настоятельно рекомендуется использовать этот механизм таблицы свойств при реализации поставщика транспорта из-за преимущества для пользователя согласованного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="631a8-108">You are strongly encouraged to use this property sheet mechanism when implementing your transport provider due to the benefit to the user of a consistent interface.</span></span>
  
## <a name="transport-providers"></a><span data-ttu-id="631a8-109">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="631a8-109">Transport providers</span></span>

<span data-ttu-id="631a8-110">Поставщики транспорта могут использовать [функцию BuildDisplayTable,](builddisplaytable.md) чтобы упростить создание таблицы отображения для использования с **DoConfigPropSheet.**</span><span class="sxs-lookup"><span data-stu-id="631a8-110">Transport providers can use the [BuildDisplayTable](builddisplaytable.md) function to simplify construction of a display table for use with **DoConfigPropSheet**.</span></span> <span data-ttu-id="631a8-111">Поставщики транспорта также могут напрямую использовать API листа свойств.</span><span class="sxs-lookup"><span data-stu-id="631a8-111">Transport providers can also use the property sheet API directly.</span></span> <span data-ttu-id="631a8-112">Для буферизации изменений свойств поставщики транспорта могут использовать [функцию CreateIProp.](createiprop.md)</span><span class="sxs-lookup"><span data-stu-id="631a8-112">To buffer changes to the properties, transport providers can use the [CreateIProp](createiprop.md) function.</span></span> <span data-ttu-id="631a8-113">Это упрощает обработку отмен пользователем, в то время как пользователь изменяет значения, хранимые в свойствах.</span><span class="sxs-lookup"><span data-stu-id="631a8-113">This simplifies the handling of cancellations by the user while the user modifies the values stored in the properties.</span></span> <span data-ttu-id="631a8-114">При необходимости поставщик транспорта также может предоставить диалоговое окно мастера для упрощения задач настройки для пользователя.</span><span class="sxs-lookup"><span data-stu-id="631a8-114">If necessary, a transport provider can also provide a wizard dialog box to simplify configuration tasks for the user.</span></span> 
  

