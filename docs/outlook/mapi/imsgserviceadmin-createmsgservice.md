---
title: Имсгсервицеадминкреатемсгсервице
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e7d30c1aba8ddc1419045c1caa8524f7d2063dc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434979"
---
# <a name="imsgserviceadmincreatemsgservice"></a><span data-ttu-id="160c2-103">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="160c2-103">IMsgServiceAdmin::CreateMsgService</span></span>

  
  
<span data-ttu-id="160c2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="160c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="160c2-105">Устаревший: рекомендуется использовать [IMsgServiceAdmin2:: креатемсгсервицеекс](imsgserviceadmin2-createmsgserviceex.md) .</span><span class="sxs-lookup"><span data-stu-id="160c2-105">Deprecated: The use of [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) is recommended.</span></span> <span data-ttu-id="160c2-106">Добавляет службу сообщений в текущий профиль.</span><span class="sxs-lookup"><span data-stu-id="160c2-106">Adds a message service to the current profile.</span></span> 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="160c2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="160c2-107">Parameters</span></span>

 <span data-ttu-id="160c2-108">_Лпсзсервице_</span><span class="sxs-lookup"><span data-stu-id="160c2-108">_lpszService_</span></span>
  
> <span data-ttu-id="160c2-109">возврата Указатель на имя добавляемой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="160c2-109">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="160c2-110">Это имя службы сообщений должно отображаться в разделе **[Services]** файла MapiSvc. INF.</span><span class="sxs-lookup"><span data-stu-id="160c2-110">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="160c2-111">_Лпсздисплайнаме_</span><span class="sxs-lookup"><span data-stu-id="160c2-111">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="160c2-112">возврата Указатель на отображаемое имя добавляемой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="160c2-112">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="160c2-113">Параметр _лпсздисплайнаме_ игнорируется, если в службе сообщений в файле MapiSvc. INF задано свойство **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="160c2-113">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="160c2-114">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="160c2-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="160c2-115">возврата Дескриптор родительского окна любых диалоговых окон или окон, которые отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="160c2-115">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="160c2-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="160c2-116">_ulFlags_</span></span>
  
> <span data-ttu-id="160c2-117">возврата Битовая маска флагов, определяющих способ установки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="160c2-117">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="160c2-118">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="160c2-118">The following flags can be set:</span></span>
    
<span data-ttu-id="160c2-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="160c2-119">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="160c2-120">Параметры Лпсзсервице и Лпсздисплайнаме должны быть приведены к LPWSTR и интерпретироваться как строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="160c2-120">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="160c2-121">СЕРВИЦЕ_НО_РЕСТАРТ_ВАРНИНГ</span><span class="sxs-lookup"><span data-stu-id="160c2-121">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="160c2-122">При добавлении новой службы сообщений в профиль подсистема MAPI на основе различных условий и условий часто определяет, что это действие требует перезапуска Outlook.</span><span class="sxs-lookup"><span data-stu-id="160c2-122">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="160c2-123">Если флаг СЕРВИЦЕ_НО_РЕСТАРТ_ВАРНИНГ не включен, а пользовательский интерфейс разрешен на основе флагов СЕРВИЦЕ_УИ_АЛВАЙС и СЕРВИЦЕ_УИ_АЛЛОВЕД, и в текущий профиль записывается по крайней мере один процесс, эта функция отображает сообщение "необходимо перезапустить Outlook для изменения вступят в силу. "</span><span class="sxs-lookup"><span data-stu-id="160c2-123">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="160c2-124">Включение флага СЕРВИЦЕ_НО_РЕСТАРТ_ВАРНИНГ подавляет отображение этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="160c2-124">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="160c2-125">СЕРВИЦЕ_УИ_АЛЛОВЕД</span><span class="sxs-lookup"><span data-stu-id="160c2-125">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="160c2-126">При необходимости вы можете использовать пользовательский интерфейс настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="160c2-126">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="160c2-127">СЕРВИЦЕ_УИ_АЛВАЙС</span><span class="sxs-lookup"><span data-stu-id="160c2-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="160c2-128">Служба сообщений отображает страницу свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="160c2-128">The message service displays its configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="160c2-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="160c2-129">Return value</span></span>

<span data-ttu-id="160c2-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="160c2-130">S_OK</span></span> 
  
> <span data-ttu-id="160c2-131">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="160c2-131">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="160c2-132">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="160c2-132">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="160c2-133">Имя службы сообщений не входит в раздел **[Services]** файла MapiSvc. INF.</span><span class="sxs-lookup"><span data-stu-id="160c2-133">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="160c2-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="160c2-134">Remarks</span></span>

<span data-ttu-id="160c2-135">Метод **имсгсервицеадмин:: креатемсгсервице** добавляет службу сообщений в текущий профиль.</span><span class="sxs-lookup"><span data-stu-id="160c2-135">The **IMsgServiceAdmin::CreateMsgService** method adds a message service to the current profile.</span></span> <span data-ttu-id="160c2-136">**Креатемсгсервице** вызывает функцию точки входа службы сообщений для выполнения определенных задач по настройке служб.</span><span class="sxs-lookup"><span data-stu-id="160c2-136">**CreateMsgService** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="160c2-137">Если в параметре _ulFlags_ ЗАДАН флаг сервице_уи_алловед, устанавливаемая служба сообщений может отображать страницу свойств, позволяющую пользователю настраивать его параметры.</span><span class="sxs-lookup"><span data-stu-id="160c2-137">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet to enable the user to configure its settings.</span></span> 
  
<span data-ttu-id="160c2-138">Файл MapiSvc. inf содержит список поставщиков, которые составляют службу сообщений и свойства для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="160c2-138">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="160c2-139">**Креатемсгсервице** сначала создает новый раздел профиля для службы сообщений, а затем копирует все сведения для этой службы из файла MapiSvc. INF в профиль, создавая новые разделы для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="160c2-139">**CreateMsgService** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="160c2-140">После того как все данные будут скопированы из MapiSvc. INF, функция точки входа службы сообщений вызывается со значением МСГ_СЕРВИЦЕ_КРЕАТЕ, установленным в параметре _улконтекст_ .</span><span class="sxs-lookup"><span data-stu-id="160c2-140">After all the information has been copied from MapiSvc.inf, the message service's entry point function is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="160c2-141">Если в параметре _ulFlags_ метода **КРЕАТЕМСГСЕРВИЦЕ** задан флаг сервице_уи_алловед, значения в параметрах _улуипарам_ и _ulFlags_ также передаются при вызове функции точки входа службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="160c2-141">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgService** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="160c2-142">Поставщики услуг должны отображать свои страницы свойств конфигурации, чтобы пользователи могли настраивать службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="160c2-142">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="160c2-143">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="160c2-143">Notes to callers</span></span>

 <span data-ttu-id="160c2-144">**Креатемсгсервице** не возвращает структуру [мапиуид](mapiuid.md) для службы сообщений, которая была добавлена в профиль.</span><span class="sxs-lookup"><span data-stu-id="160c2-144">**CreateMsgService** does not return the [MAPIUID](mapiuid.md) structure for the message service that was added to the profile.</span></span> 
  
<span data-ttu-id="160c2-145">Чтобы получить **мапиуид** для созданной службы сообщений, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="160c2-145">To retrieve the **MAPIUID** for the created message service, use the following procedure:</span></span> 
  
1. <span data-ttu-id="160c2-146">ВыЗовите метод [имсгсервицеадмин:: жетмсгсервицетабле](imsgserviceadmin-getmsgservicetable.md) , чтобы получить таблицу администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="160c2-146">Call the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method to get the message service administration table.</span></span> 
    
2. <span data-ttu-id="160c2-147">Чтобы определить строку, представляющую службу сообщений, разместите в таблице ограничение, соответствующее свойству **пр_сервице_наме** ([PidTagServiceName](pidtagservicename-canonical-property.md)) с именем службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="160c2-147">Locate the row that represents the message service by placing a restriction on the table that matches the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property with the name of the message service.</span></span> 
    
3. <span data-ttu-id="160c2-148">Получите свойство **пр_сервице_уид** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) службы.</span><span class="sxs-lookup"><span data-stu-id="160c2-148">Retrieve the service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span> 
    
4. <span data-ttu-id="160c2-149">Передайте значение свойства **пр_сервице_уид** в параметре _Лпуид_ в метод [имсгсервицеадмин:: конфигуремсгсервице](imsgserviceadmin-configuremsgservice.md) для настройки службы.</span><span class="sxs-lookup"><span data-stu-id="160c2-149">Pass the value of the **PR_SERVICE_UID** property in the  _lpUid_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
    
> [!CAUTION]
> <span data-ttu-id="160c2-150">Реализация подсистемы MAPI для Microsoft Outlook 2010 не поддерживает МАПИ_УНИКОДЕ и не будет работать, если она используется.</span><span class="sxs-lookup"><span data-stu-id="160c2-150">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="160c2-151">_UlFlags_ сервице_но_рестарт_варнинг может быть не определен в текущем загружаемом файле заголовке, в таком случае его можно добавить в код, используя следующее значение: _гт_`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="160c2-151">The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="160c2-152">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="160c2-152">MFCMAPI reference</span></span>

<span data-ttu-id="160c2-153">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="160c2-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="160c2-154">**Файл**</span><span class="sxs-lookup"><span data-stu-id="160c2-154">**File**</span></span>|<span data-ttu-id="160c2-155">**Функция**</span><span class="sxs-lookup"><span data-stu-id="160c2-155">**Function**</span></span>|<span data-ttu-id="160c2-156">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="160c2-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="160c2-157">Мапипрофилефунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="160c2-157">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="160c2-158">Храддсервицетопрофиле</span><span class="sxs-lookup"><span data-stu-id="160c2-158">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="160c2-159">MFCMAPI использует метод **имсгсервицеадмин:: креатемсгсервице** , чтобы добавить службу в профиль.</span><span class="sxs-lookup"><span data-stu-id="160c2-159">MFCMAPI uses the **IMsgServiceAdmin::CreateMsgService** method to add a service to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="160c2-160">См. также</span><span class="sxs-lookup"><span data-stu-id="160c2-160">See also</span></span>



[<span data-ttu-id="160c2-161">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="160c2-161">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="160c2-162">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="160c2-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

