---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b7fe25491228f00f6865af963db36f27bae5d7a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410184"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a><span data-ttu-id="3b7ae-103">IMsgServiceAdmin2::CreateMsgServiceEx</span><span class="sxs-lookup"><span data-stu-id="3b7ae-103">IMsgServiceAdmin2::CreateMsgServiceEx</span></span>

  
  
<span data-ttu-id="3b7ae-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b7ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b7ae-105">Добавляет службу сообщений в текущий профиль и возвращает только что добавленный идентификатор UID службы.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-105">Adds a message service to the current profile and returns that newly added service UID.</span></span>
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a><span data-ttu-id="3b7ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b7ae-106">Parameters</span></span>

 <span data-ttu-id="3b7ae-107">_Лпсзсервице_</span><span class="sxs-lookup"><span data-stu-id="3b7ae-107">_lpszService_</span></span>
  
> <span data-ttu-id="3b7ae-108">возврата Указатель на имя добавляемой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-108">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="3b7ae-109">Это имя службы сообщений должно отображаться в разделе **[Services]** файла MapiSvc. INF.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-109">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="3b7ae-110">_Лпсздисплайнаме_</span><span class="sxs-lookup"><span data-stu-id="3b7ae-110">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="3b7ae-111">возврата Указатель на отображаемое имя добавляемой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-111">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="3b7ae-112">Параметр _лпсздисплайнаме_ игнорируется, если в службе сообщений в файле MapiSvc. INF задано свойство **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3b7ae-112">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="3b7ae-113">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="3b7ae-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="3b7ae-114">возврата Дескриптор родительского окна любых диалоговых окон или окон, которые отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="3b7ae-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3b7ae-115">_ulFlags_</span></span>
  
> <span data-ttu-id="3b7ae-116">возврата Битовая маска флагов, определяющих способ установки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-116">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="3b7ae-117">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="3b7ae-117">The following flags can be set:</span></span>
    
<span data-ttu-id="3b7ae-118">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3b7ae-118">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="3b7ae-119">Параметры Лпсзсервице и Лпсздисплайнаме должны быть приведены к LPWSTR и интерпретироваться как строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-119">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="3b7ae-120">СЕРВИЦЕ_НО_РЕСТАРТ_ВАРНИНГ</span><span class="sxs-lookup"><span data-stu-id="3b7ae-120">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="3b7ae-121">При добавлении новой службы сообщений в профиль подсистема MAPI на основе различных условий и условий часто определяет, что это действие требует перезапуска Outlook.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-121">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="3b7ae-122">Если флаг СЕРВИЦЕ_НО_РЕСТАРТ_ВАРНИНГ не включен, а пользовательский интерфейс разрешен на основе флагов СЕРВИЦЕ_УИ_АЛВАЙС и СЕРВИЦЕ_УИ_АЛЛОВЕД, и в текущий профиль записывается по крайней мере один процесс, эта функция отображает сообщение "необходимо перезапустить Outlook для изменения вступят в силу. "</span><span class="sxs-lookup"><span data-stu-id="3b7ae-122">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="3b7ae-123">Включение флага СЕРВИЦЕ_НО_РЕСТАРТ_ВАРНИНГ подавляет отображение этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-123">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="3b7ae-124">СЕРВИЦЕ_УИ_АЛЛОВЕД</span><span class="sxs-lookup"><span data-stu-id="3b7ae-124">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="3b7ae-125">При необходимости вы можете использовать пользовательский интерфейс настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-125">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="3b7ae-126">СЕРВИЦЕ_УИ_АЛВАЙС</span><span class="sxs-lookup"><span data-stu-id="3b7ae-126">SERVICE_UI_ALWAYS</span></span>
  
> <span data-ttu-id="3b7ae-127">Служба сообщений отображает страницу свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-127">The message service displays its configuration property sheet.</span></span>
    
 <span data-ttu-id="3b7ae-128">_Лпуидсервице_</span><span class="sxs-lookup"><span data-stu-id="3b7ae-128">_lpuidService_</span></span>
  
> <span data-ttu-id="3b7ae-129">вышли Указатель на идентификатор UID службы сообщений добавлен.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-129">[out] The pointer to the UID of the message service added.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3b7ae-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b7ae-130">Return value</span></span>

<span data-ttu-id="3b7ae-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b7ae-131">S_OK</span></span>
  
> <span data-ttu-id="3b7ae-132">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-132">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="3b7ae-133">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="3b7ae-133">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="3b7ae-134">Имя службы сообщений не входит в раздел **[Services]** файла MapiSvc. INF.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-134">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3b7ae-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="3b7ae-135">Remarks</span></span>

<span data-ttu-id="3b7ae-136">Метод **IMsgServiceAdmin2:: креатемсгсервицеекс** добавляет службу сообщений в текущий профиль.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-136">The **IMsgServiceAdmin2::CreateMsgServiceEx** method adds a message service to the current profile.</span></span> <span data-ttu-id="3b7ae-137">**Креатемсгсервицеекс** вызывает функцию точки входа службы сообщений для выполнения определенных задач по настройке служб.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-137">**CreateMsgServiceEx** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="3b7ae-138">Если в параметре _ulFlags_ ЗАДАН флаг сервице_уи_алловед, устанавливаемая служба сообщений может отображать лист свойств, позволяющий пользователю настраивать его параметры.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-138">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet enabling the user to configure its settings.</span></span> 
  
<span data-ttu-id="3b7ae-139">Файл MapiSvc. inf содержит список поставщиков, которые составляют службу сообщений и свойства для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-139">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="3b7ae-140">**Креатемсгсервицеекс** сначала создает новый раздел профиля для службы сообщений, а затем копирует все сведения для этой службы из файла MapiSvc. INF в профиль, создавая новые разделы для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-140">**CreateMsgServiceEx** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="3b7ae-141">После того как все данные будут скопированы из MapiSvc. INF, функция точки входа службы сообщений, **мсгсервицеентри**, вызывается со значением мсг_сервице_креате, установленным в параметре _улконтекст_ .</span><span class="sxs-lookup"><span data-stu-id="3b7ae-141">After all the information has been copied from MapiSvc.inf, the message service's entry point function, **MSGSERVICEENTRY**, is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="3b7ae-142">Если в параметре _ulFlags_ метода **КРЕАТЕМСГСЕРВИЦЕЕКС** задан флаг сервице_уи_алловед, значения в параметрах _улуипарам_ и _ulFlags_ также передаются при вызове функции точки входа службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-142">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgServiceEx** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="3b7ae-143">Поставщики услуг должны отображать свои страницы свойств конфигурации, чтобы пользователи могли настраивать службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-143">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3b7ae-144">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="3b7ae-144">Notes to callers</span></span>

<span data-ttu-id="3b7ae-145">Если аргумент \*\*\*\* _ЛПУИДСЕРВИЦЕ_ креатемсгсервицеекс имеет значение, отличное от NULL, свойство **пр_сервице_уид** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) службы сообщений, добавленНой в профиль, возвращается в **идентификаторе GUID** , на который указывает эта точка.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-145">If the **CreateMsgServiceEx** _lpuidService_ argument is not NULL, the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property of the message service that was added to the profile is returned in the **GUID** to which it points.</span></span> 
  
<span data-ttu-id="3b7ae-146">Передайте значение свойства **пр_сервице_уид** в параметре _Лпуидсервице_ в метод [имсгсервицеадмин:: конфигуремсгсервице](imsgserviceadmin-configuremsgservice.md) для настройки службы.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-146">Pass the value of the **PR_SERVICE_UID** property in the  _lpuidService_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="3b7ae-147">Реализация подсистемы MAPI для Microsoft Outlook 2010 не поддерживает МАПИ_УНИКОДЕ и не будет работать, если она используется.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-147">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="3b7ae-148">Интерфейс IMsgServiceAdmin2 предоставляется одним и тем же объектом, который реализует интерфейс Имсгсервицеадмин, и доступен с помощью реализации Outlook подсистемы MAPI с момента создания Outlook 2003.</span><span class="sxs-lookup"><span data-stu-id="3b7ae-148">The IMsgServiceAdmin2 interface is exposed by the same object that implements the IMsgServiceAdmin interface, and has been available using Outlook's implementation of the MAPI subsystem since Outlook 2003.</span></span> <span data-ttu-id="3b7ae-149">Его IID определяется следующим образом `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`: _гт_ _гт_ _ulFlags_ сервице_но_рестарт_варнинг может быть не определен в файле заголовков, доступных для загрузки, в этом случае можно добавить его в код, используя следующее значение: _гт_`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="3b7ae-149">Its IID is defined as follows: >  `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)`>  `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3b7ae-150">См. также</span><span class="sxs-lookup"><span data-stu-id="3b7ae-150">See also</span></span>



[<span data-ttu-id="3b7ae-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span><span class="sxs-lookup"><span data-stu-id="3b7ae-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span></span>](imsgserviceadmin2imsgserviceadmin.md)


[<span data-ttu-id="3b7ae-152">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="3b7ae-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

