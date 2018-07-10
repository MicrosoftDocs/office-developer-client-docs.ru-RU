---
title: Макрос КЭлементуУправления (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: КЭлементуУправления можно использовать для перемещения фокуса на указанный элемент управления в текущей записи открыть представление.
ms.openlocfilehash: ec156d1eb6c510ee38c0268a7b0f51bdde80f887
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806945"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a><span data-ttu-id="00ca4-103">Макрос КЭлементуУправления (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="00ca4-103">GoToControl Macro Action (Access custom web app)</span></span>

<span data-ttu-id="00ca4-104">**КЭлементуУправления** можно использовать для перемещения фокуса на указанный элемент управления в текущей записи открыть представление.</span><span class="sxs-lookup"><span data-stu-id="00ca4-104">You can use the **GoToControl** action to move the focus to the specified control in the current record of the open view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="00ca4-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="00ca4-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="00ca4-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="00ca4-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="00ca4-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="00ca4-107">Setting</span></span>

<span data-ttu-id="00ca4-108">**КЭлементуУправления** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="00ca4-108">The **GoToControl** action has the following argument.</span></span> 
  
|<span data-ttu-id="00ca4-109">**Аргумент действия**</span><span class="sxs-lookup"><span data-stu-id="00ca4-109">**Action argument**</span></span>|<span data-ttu-id="00ca4-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="00ca4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00ca4-111">**Имя элемента управления**</span><span class="sxs-lookup"><span data-stu-id="00ca4-111">**Control Name**</span></span> <br/> |<span data-ttu-id="00ca4-112">Имя поля или элемента управления, где будут фокус.</span><span class="sxs-lookup"><span data-stu-id="00ca4-112">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="00ca4-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="00ca4-113">This is a required argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00ca4-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="00ca4-114">Remarks</span></span>

<span data-ttu-id="00ca4-115">Это действие можно использовать отдельного поля или элемент управления имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="00ca4-115">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="00ca4-116">Это действие также можно использовать для перехода в форме при выполнении определенных условий.</span><span class="sxs-lookup"><span data-stu-id="00ca4-116">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="00ca4-117">Например, если пользователь вводит нет в элемента управления в форме медицинского страхования, фокус автоматически можно пропустить управления имя супруга/партнера и перемещение к следующему элементу управления.</span><span class="sxs-lookup"><span data-stu-id="00ca4-117">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>
  

