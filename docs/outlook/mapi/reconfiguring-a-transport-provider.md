---
title: Перенастройка поставщика транспорта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b35ca2bb52439cf2ba1750c6fad2883730c4c3f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408413"
---
# <a name="reconfiguring-a-transport-provider"></a><span data-ttu-id="f4251-103">Перенастройка поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="f4251-103">Reconfiguring a Transport Provider</span></span>

  
  
<span data-ttu-id="f4251-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4251-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4251-105">Вы можете использовать объект состояния поставщика транспорта, чтобы изменить некоторые свойства поставщика.</span><span class="sxs-lookup"><span data-stu-id="f4251-105">You can use a transport provider's status object to change some of the properties of the provider.</span></span> <span data-ttu-id="f4251-106">Диапазон свойств, которые можно изменить, зависит от свойств, которые включены в страницу свойств поставщика, и от того, как эти свойства определены.</span><span class="sxs-lookup"><span data-stu-id="f4251-106">The range of properties that can be changed depends on the properties that are included with the provider's property sheet and how those properties are defined.</span></span> 
  
 <span data-ttu-id="f4251-107">**Повторная настройка активного поставщика транспорта**</span><span class="sxs-lookup"><span data-stu-id="f4251-107">**To reconfigure an active transport provider**</span></span>
  
1. <span data-ttu-id="f4251-108">Call [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для доступа к таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="f4251-108">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="f4251-109">Укажите строку для поставщика транспорта, которую необходимо изменить, создав ограничение свойства, которое соответствует **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) с именем целевого поставщика.</span><span class="sxs-lookup"><span data-stu-id="f4251-109">Locate the row for the transport provider to be reconfigured by creating a property restriction that matches **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the target provider.</span></span> 
    
3. <span data-ttu-id="f4251-110">Call [IMAPITable:: FindRow](imapitable-findrow.md) для получения соответствующей строки.</span><span class="sxs-lookup"><span data-stu-id="f4251-110">Call [IMAPITable::FindRow](imapitable-findrow.md) to retrieve the appropriate row.</span></span> 
    
4. <span data-ttu-id="f4251-111">Убедитесь, что флаги СТАТУС_СЕТТИНГС_ДИАЛОГ и СТАТУС_ВАЛИДАТЕ_СТАТЕ установлены в свойстве **пр_ресаурце_месодс** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) целевого поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="f4251-111">Check that the STATUS_SETTINGS_DIALOG and STATUS_VALIDATE_STATE flags are set in the target transport provider's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span> <span data-ttu-id="f4251-112">Если СТАТУС_СЕТТИНГС_ДИАЛОГ не задано, то поставщик транспорта не отображает страницу свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f4251-112">If STATUS_SETTINGS_DIALOG is not set, the transport provider does not display a configuration property sheet.</span></span> <span data-ttu-id="f4251-113">Если СТАТУС_ВАЛИДАТЕ_СТАТЕ не задано, невозможно выполнить динамическую перенастройку.</span><span class="sxs-lookup"><span data-stu-id="f4251-113">If STATUS_VALIDATE_STATE is not set, you cannot perform dynamic reconfiguration.</span></span>
    
5. <span data-ttu-id="f4251-114">Если задано значение СТАТУС_СЕТТИНГС_ДИАЛОГ, вызовите [имапистатус:: сеттингсдиалог](imapistatus-settingsdialog.md) , чтобы отобразить лист свойств поставщика транспорта и разрешить пользователю вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="f4251-114">If STATUS_SETTINGS_DIALOG is set, call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the transport provider's property sheet and allow the user to make changes.</span></span> 
    
6. <span data-ttu-id="f4251-115">Когда пользователь завершит перенастройку, вызовите метод [имапистатус:: валидатестате](imapistatus-validatestate.md) , если статус_валидате_стате задано, передает конфиг_чанжед.</span><span class="sxs-lookup"><span data-stu-id="f4251-115">After the user has finished with the reconfiguration, call [IMAPIStatus::ValidateState](imapistatus-validatestate.md) if STATUS_VALIDATE_STATE is set, passing CONFIG_CHANGED.</span></span> 
    

