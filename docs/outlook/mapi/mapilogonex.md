---
title: MAPILogonEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPILogonEx
api_type:
- HeaderDef
ms.assetid: 98091e5b-1abd-4814-9c7a-583b420ee11d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9f2ec8f0ec00f7314982e9b112415f69901c358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424121"
---
# <a name="mapilogonex"></a><span data-ttu-id="6cc8c-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="6cc8c-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="6cc8c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cc8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cc8c-105">Занося клиентские приложения в сеанс с системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6cc8c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6cc8c-106">Header file:</span></span>  <br/> |<span data-ttu-id="6cc8c-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="6cc8c-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="6cc8c-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="6cc8c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6cc8c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6cc8c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6cc8c-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="6cc8c-110">Called by:</span></span>  <br/> |<span data-ttu-id="6cc8c-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="6cc8c-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="6cc8c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cc8c-112">Parameters</span></span>

 <span data-ttu-id="6cc8c-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6cc8c-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="6cc8c-114">[in] Обработать окно, в котором диалоговое окно для логотипа является модальным.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="6cc8c-115">Если во время вызова диалоговое окно не отображается, параметр  _ulUIParam_ игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="6cc8c-116">Этот параметр может быть нулем.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="6cc8c-117">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="6cc8c-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="6cc8c-118">[in] Указатель на строку, которая содержит имя профиля, используемого при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="6cc8c-119">Эта строка может быть ограничена 64 символами.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="6cc8c-120">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="6cc8c-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="6cc8c-121">[in] Указатель на строку, содержаную пароль профиля.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="6cc8c-122">Параметр  _lpszPassword должен_ иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="6cc8c-123">_flFlags_</span><span class="sxs-lookup"><span data-stu-id="6cc8c-123">_flFlags_</span></span>
  
> <span data-ttu-id="6cc8c-124">[in] Битоваяmas флагов, используемых для управления выполнением логово.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="6cc8c-125">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="6cc8c-125">The following flags can be set:</span></span>
    
<span data-ttu-id="6cc8c-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="6cc8c-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="6cc8c-127">Должен быть возвращен общий сеанс, который позволяет последующим клиентам получить сеанс без предоставления учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="6cc8c-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="6cc8c-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="6cc8c-129">Войдите в сеанс и запустите все операции в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="6cc8c-130">В общем случае, если клиент собирается обрабатывать фоновый поток или отдельный процесс ненавязчивым для потока переднего плана, он должен вызвать флаг MAPI_BG_SESSION.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="6cc8c-131">Клиентские приложения, такие как механизм индексации или открытие файла личных папок (PST) для доступа к фоновому типу, являются примерами использования MAPI_BG_SESSION. MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="6cc8c-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="6cc8c-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="6cc8c-133">Профиль по умолчанию не следует использовать, и пользователю необходимо предоставить профиль.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="6cc8c-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="6cc8c-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="6cc8c-135">Войдите с расширенными возможностями.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-135">Log on with extended capabilities.</span></span> <span data-ttu-id="6cc8c-136">Этот флаг всегда должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-136">This flag should always be set.</span></span>
    
<span data-ttu-id="6cc8c-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="6cc8c-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="6cc8c-138">Перед возвратом необходимо попытаться скачать все сообщения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="6cc8c-139">Если флаг MAPI_FORCE_DOWNLOAD не установлен, сообщения можно скачать в фоновом режиме после возврата вызова MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="6cc8c-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="6cc8c-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="6cc8c-141">При необходимости должно отобразиться диалоговое окно с запросом у пользователя сведений о пользователе.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="6cc8c-142">Если флаг MAPI_LOGON_UI не установлен, клиент вызова не отображает диалоговое окно входа и возвращает значение ошибки, если пользователь не вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="6cc8c-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="6cc8c-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="6cc8c-144">Вместо получения общего сеанса необходимо попытаться создать новый сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="6cc8c-145">Если флаг MAPI_NEW_SESSION не установлен, MAPILogonEx использует существующий общий сеанс, даже если параметр  _lpszprofileName_ не имеет NULL.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="6cc8c-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="6cc8c-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="6cc8c-147">MAPI не должен сообщать пулу MAPI о существовании сеанса.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="6cc8c-148">В результате в сеансе не может быть отправлено или получено ни одного сообщения, кроме как через тесно сопряженное хранилище и пару транспорта.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="6cc8c-149">Вызывающий клиент устанавливает этот флаг, если он действует как агент, если необходимо сделать настройку или если клиент просматривает доступные хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="6cc8c-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="6cc8c-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="6cc8c-151">Вызываемая служба работает как служба Windows.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="6cc8c-152">Вызывателям, которые не работают в качестве службы Windows, не следует устанавливать этот флаг; вызыватели, работающие в качестве службы, должны установить этот флаг.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="6cc8c-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="6cc8c-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="6cc8c-154">MapILogonEx должен отображать диалоговое окно конфигурации для каждой службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="6cc8c-155">Диалоговые окна отображаются после того, как профиль был выбран, но до входа в систему какой-либо службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="6cc8c-156">Общее диалоговое окно MAPI для регистрации также содержит поле, которое запрашивает ту же операцию.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="6cc8c-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="6cc8c-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="6cc8c-158">Если он заблокирован более чем на несколько секунд, то при этом не удастся при этом.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="6cc8c-159">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6cc8c-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6cc8c-160">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="6cc8c-161">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="6cc8c-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6cc8c-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="6cc8c-163">Подсистема обмена сообщениями должна заменить имя профиля по умолчанию для параметра _lpszProfileName._</span><span class="sxs-lookup"><span data-stu-id="6cc8c-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="6cc8c-164">Флаг MAPI_EXPLICIT_PROFILE игнорируется, если  _lpszProfileName_ не имеет NULL или не пуст.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="6cc8c-165">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="6cc8c-165">_lppSession_</span></span>
  
> <span data-ttu-id="6cc8c-166">[out] Указатель на указатель на интерфейс сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6cc8c-167">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6cc8c-167">Return value</span></span>

<span data-ttu-id="6cc8c-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="6cc8c-168">S_OK</span></span> 
  
> <span data-ttu-id="6cc8c-169">Успешно вошел в окну.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-169">The logon succeeded.</span></span>
    
<span data-ttu-id="6cc8c-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="6cc8c-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="6cc8c-171">Неудача при запуске из-за того, что один или несколько параметров MAPILogonEx недействительны, или из-за того, что открыто слишком много сеансов.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="6cc8c-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6cc8c-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="6cc8c-173">MAPI сериализует все ведомости с помощью мьютэкса.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="6cc8c-174">Возвращается, если флаг MAPI_TIMEOUT_SHORT установлен, а другой поток удерживает мьюex.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="6cc8c-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="6cc8c-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="6cc8c-176">Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6cc8c-177">Примечания</span><span class="sxs-lookup"><span data-stu-id="6cc8c-177">Remarks</span></span>

<span data-ttu-id="6cc8c-178">Клиентские приложения MAPI звонят функции MAPILogonEx для входа в сеанс с системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="6cc8c-179">Все строки, которые передаются и возвращаются в вызовы MAPI, завершаются с нулью и должны быть указаны в текущем наборе символов или кодовой странице операционной системы вызываемого клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="6cc8c-180">Параметр  _lpszProfileName_ игнорируется, если существует предыдущий сеанс, который назывался MapiLogonEx с установленным флагом MAPI_ALLOW_OTHERS и если флаг MAPI_NEW_SESSION не установлен.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="6cc8c-181">Если параметр  _lpszProfileName_ имеет NULL или указывает на пустую строку, а параметр  _flFlags_ содержит флаг MAPI_LOGON_UI, функция MAPILogonEx создает диалоговое окно для логотипа с пустым полем для имени профиля.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="6cc8c-182">При входе в определенный профиль клиент должен передать флаг MAPI_NEW_SESSION mapILogonEx в дополнение к имени профиля.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="6cc8c-183">В противном случае, если другой клиент установил общий сеанс, войдя в систему с помощью MAPI_ALLOW_OTHERS, клиент будет вошел в общий сеанс, а не в запрашиваемом профиле.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="6cc8c-184">Флаг MAPI_EXPLICIT_PROFILE не вызывает использования имени профиля по умолчанию, если  _lpszProfileName_ имеет значение NULL или пуст, если MAPI_USE_DEFAULT флага также присутствует.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="6cc8c-185">Флаг MAPI_NO_MAIL имеет несколько эффектов, которые приводят к следующим последствиям, если не используется пулер MAPI:</span><span class="sxs-lookup"><span data-stu-id="6cc8c-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="6cc8c-186">В ходе этого сеанса пул mapI не может отправлять и не доставлять сообщения.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="6cc8c-187">Отправлять и доставлять сообщения могут только тесно сжатые поставщики услуг хранения и транспорта.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="6cc8c-188">Серверные хранилища могут по-прежнему отправлять или доставлять сообщения.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="6cc8c-189">Сообщения, отправленные или доставленные серверным хранилищам, не обрабатываются ни одной службой обработки.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="6cc8c-190">Параметры транспорта для каждого сообщения и получателя недоступны.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="6cc8c-191">Таблица состояния не содержит записей для поставщиков транспорта, и все функции транспорта, зависящие от объектов состояния (например, конфигурации), недоступны.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="6cc8c-192">Строка пула сообщений в таблице состояния содержит STATUS_FAILURE сообщения.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="6cc8c-193">Разрешены висячие ветви, но они не приводят к тому, что предыдущий при этом не будет получать обновления объектов состояния.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="6cc8c-194">Служба всегда должна входить в систему с помощью MAPI_NO_MAIL флага.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6cc8c-195">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6cc8c-195">MFCMAPI reference</span></span>

<span data-ttu-id="6cc8c-196">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6cc8c-197">**Файл**</span><span class="sxs-lookup"><span data-stu-id="6cc8c-197">**File**</span></span>|<span data-ttu-id="6cc8c-198">**Функция**</span><span class="sxs-lookup"><span data-stu-id="6cc8c-198">**Function**</span></span>|<span data-ttu-id="6cc8c-199">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="6cc8c-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6cc8c-200">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="6cc8c-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="6cc8c-201">CMapiObjects::MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="6cc8c-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="6cc8c-202">MFCMAPI использует метод MAPILogonEx для входа в MAPI.</span><span class="sxs-lookup"><span data-stu-id="6cc8c-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6cc8c-203">См. также</span><span class="sxs-lookup"><span data-stu-id="6cc8c-203">See also</span></span>



[<span data-ttu-id="6cc8c-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="6cc8c-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="6cc8c-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="6cc8c-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="6cc8c-206">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="6cc8c-206">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

