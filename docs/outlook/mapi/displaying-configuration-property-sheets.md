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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316403"
---
# <a name="displaying-configuration-property-sheets"></a><span data-ttu-id="02b53-103">Отображение страниц свойств конфигурации</span><span class="sxs-lookup"><span data-stu-id="02b53-103">Displaying configuration property sheets</span></span>

<span data-ttu-id="02b53-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02b53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02b53-105">Поставщики транспорта используют метод [имаписуппорт::D оконфигпропшит](imapisupport-doconfigpropsheet.md) для реализации страниц свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="02b53-105">Transport providers use the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to implement configuration property sheets.</span></span> <span data-ttu-id="02b53-106">При вызове **доконфигпропшит**поставщик транспорта передает указатель на массив свойств вместе со сведениями о том, как их отображать.</span><span class="sxs-lookup"><span data-stu-id="02b53-106">When calling **DoConfigPropSheet**, the transport provider passes in a pointer to an array of properties along with information about how to display them.</span></span> <span data-ttu-id="02b53-107">После этого MAPI отображает свойства для пользователя, используя стандартное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="02b53-107">MAPI then presents the properties to the user by means of a standard dialog box.</span></span> <span data-ttu-id="02b53-108">Настоятельно рекомендуется использовать этот механизм страниц свойств при реализации поставщика транспорта, так как он дает преимущество для согласованного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="02b53-108">You are strongly encouraged to use this property sheet mechanism when implementing your transport provider due to the benefit to the user of a consistent interface.</span></span>
  
## <a name="transport-providers"></a><span data-ttu-id="02b53-109">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="02b53-109">Transport providers</span></span>

<span data-ttu-id="02b53-110">Поставщики транспорта могут использовать функцию [буилддисплайтабле](builddisplaytable.md) для упрощения создания таблицы отображения для использования с **доконфигпропшит**.</span><span class="sxs-lookup"><span data-stu-id="02b53-110">Transport providers can use the [BuildDisplayTable](builddisplaytable.md) function to simplify construction of a display table for use with **DoConfigPropSheet**.</span></span> <span data-ttu-id="02b53-111">Поставщики транспорта также могут использовать API листа свойств напрямую.</span><span class="sxs-lookup"><span data-stu-id="02b53-111">Transport providers can also use the property sheet API directly.</span></span> <span data-ttu-id="02b53-112">Чтобы внести изменения в буфер для изменения свойств, поставщики транспорта могут использовать функцию [креатеипроп](createiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="02b53-112">To buffer changes to the properties, transport providers can use the [CreateIProp](createiprop.md) function.</span></span> <span data-ttu-id="02b53-113">Это упрощает обработку отмен пользователем, в то время как пользователь изменяет значения, хранящиеся в свойствах.</span><span class="sxs-lookup"><span data-stu-id="02b53-113">This simplifies the handling of cancellations by the user while the user modifies the values stored in the properties.</span></span> <span data-ttu-id="02b53-114">При необходимости поставщик транспорта также может предоставить диалоговое окно мастера для упрощения задач по настройке пользователя.</span><span class="sxs-lookup"><span data-stu-id="02b53-114">If necessary, a transport provider can also provide a wizard dialog box to simplify configuration tasks for the user.</span></span> 
  

