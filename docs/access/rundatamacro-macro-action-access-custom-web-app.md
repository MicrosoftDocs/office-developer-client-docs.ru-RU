---
title: Макрос ЗапускМакросаДанных (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: ЗапускМакросаДанных можно использовать для запуска автономного макроса данных.
ms.openlocfilehash: 55a0ff4c731dc517c5d71aa20d8e46c3b4ff4611
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807103"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a><span data-ttu-id="5ef83-103">Макрос ЗапускМакросаДанных (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="5ef83-103">RunDataMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="5ef83-104">**ЗапускМакросаДанных** можно использовать для запуска автономного макроса данных.</span><span class="sxs-lookup"><span data-stu-id="5ef83-104">You can use the **RunDataMacro** action to run a standalone data macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5ef83-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5ef83-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="5ef83-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="5ef83-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="5ef83-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ef83-107">Setting</span></span>

<span data-ttu-id="5ef83-108">**ЗапускМакросаДанных** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="5ef83-108">The **RunDataMacro** action has the following argument.</span></span> 
  
|<span data-ttu-id="5ef83-109">**Аргумент действия**</span><span class="sxs-lookup"><span data-stu-id="5ef83-109">**Action argument**</span></span>|<span data-ttu-id="5ef83-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5ef83-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5ef83-111">_Имя макроса_</span><span class="sxs-lookup"><span data-stu-id="5ef83-111">_Macro Name_</span></span> <br/> |<span data-ttu-id="5ef83-112">Имя макроса данных для запуска.</span><span class="sxs-lookup"><span data-stu-id="5ef83-112">The name of the data macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ef83-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="5ef83-113">Remarks</span></span>

<span data-ttu-id="5ef83-114">При выборе макрос данных, которая должна работать в конструктор макросов Access определяет необходимость в макрос данных параметров.</span><span class="sxs-lookup"><span data-stu-id="5ef83-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="5ef83-115">Если макрос данных требуются параметры, текстовых полей отображаются для ввода в аргументах.</span><span class="sxs-lookup"><span data-stu-id="5ef83-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>
  
<span data-ttu-id="5ef83-116">При запуске макроса, содержащего **ЗапускМакросаДанных** и достигает **ЗапускМакросаДанных** , Access запускает макрос называемое данных.</span><span class="sxs-lookup"><span data-stu-id="5ef83-116">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro.</span></span> <span data-ttu-id="5ef83-117">По завершении макрос называемое данных Access возвращает исходное макрос и выполняется следующее действие.</span><span class="sxs-lookup"><span data-stu-id="5ef83-117">When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span> 
  

