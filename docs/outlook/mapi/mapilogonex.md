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
# <a name="mapilogonex"></a><span data-ttu-id="e6c3f-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="e6c3f-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="e6c3f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6c3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6c3f-105">Журналы клиентского приложения на сеанс с системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6c3f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e6c3f-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6c3f-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="e6c3f-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="e6c3f-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="e6c3f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e6c3f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e6c3f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e6c3f-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="e6c3f-110">Called by:</span></span>  <br/> |<span data-ttu-id="e6c3f-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="e6c3f-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="e6c3f-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="e6c3f-112">Parameters</span></span>

 <span data-ttu-id="e6c3f-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e6c3f-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="e6c3f-114">[in] Ручка к окну, к которому диалоговое окно логотипа является модальным.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="e6c3f-115">Если во время вызова диалоговое окно не отображается,  _параметр ulUIParam_ игнорируется.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="e6c3f-116">Этот параметр может быть нулем.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="e6c3f-117">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="e6c3f-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="e6c3f-118">[in] Указатель на строку, которая содержит имя профиля, используемого при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="e6c3f-119">Эта строка ограничена 64 символами.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="e6c3f-120">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="e6c3f-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="e6c3f-121">[in] Указатель на строку, содержаную пароль профиля.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="e6c3f-122">Параметр  _lpszPassword должен_ быть NULL.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="e6c3f-123">_flFlags_</span><span class="sxs-lookup"><span data-stu-id="e6c3f-123">_flFlags_</span></span>
  
> <span data-ttu-id="e6c3f-124">[in] Bitmask флагов, используемых для управления выполнением логотипа.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="e6c3f-125">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="e6c3f-125">The following flags can be set:</span></span>
    
<span data-ttu-id="e6c3f-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="e6c3f-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="e6c3f-127">Общий сеанс должен быть возвращен, что позволяет более поздним клиентам получать сеанс без предоставления учетных данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="e6c3f-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="e6c3f-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="e6c3f-129">Войдите в сеанс и запустите все операции в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="e6c3f-130">В общем случае, если клиент намерен делать обработку на фоновом потоке или в отдельном процессе ненавязчивым для переднего плана потоком, он должен вызывать его с MAPI_BG_SESSION флагом.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="e6c3f-131">Клиентские приложения, такие как двигатель индексации или открытие файла персональных папок (PST) для доступа к фоновому типу, являются примерами использования MAPI_BG_SESSION. MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="e6c3f-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="e6c3f-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="e6c3f-133">Не следует использовать профиль по умолчанию, и пользователю необходимо предоставить профиль.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="e6c3f-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="e6c3f-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="e6c3f-135">Войдите в систему с расширенными возможностями.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-135">Log on with extended capabilities.</span></span> <span data-ttu-id="e6c3f-136">Этот флаг всегда должен быть заданной.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-136">This flag should always be set.</span></span>
    
<span data-ttu-id="e6c3f-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="e6c3f-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="e6c3f-138">Перед возвращением необходимо скачать все сообщения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="e6c3f-139">Если флаг MAPI_FORCE_DOWNLOAD не установлен, сообщения можно скачать в фоновом режиме после возврата вызова в MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="e6c3f-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="e6c3f-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="e6c3f-141">Диалоговое окно должно отображаться, чтобы при необходимости подсказыть пользователю сведения о логотипе.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="e6c3f-142">Если флаг MAPI_LOGON_UI не установлен, клиент-вызов не отображает диалоговое окно с логотипом и возвращает значение ошибки, если пользователь не вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="e6c3f-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="e6c3f-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="e6c3f-144">Следует предпринять попытку создания нового сеанса MAPI вместо приобретения общего сеанса.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="e6c3f-145">Если флаг MAPI_NEW_SESSION не установлен, MAPILogonEx использует существующий общий сеанс, даже если параметр  _lpszprofileName_ не является NULL.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="e6c3f-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="e6c3f-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="e6c3f-147">MAPI не должна информировать шпалер MAPI о существовании сеанса.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="e6c3f-148">В результате в сеансе не может быть отправлено или получено сообщение, за исключением тесной пары магазинов и транспорта.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="e6c3f-149">Клиент-вызов задает этот флаг, если он действует как агент, если необходимо сделать работу по настройке или если клиент просматривает доступные хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="e6c3f-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="e6c3f-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="e6c3f-151">Вызываемая служба работает в качестве Windows службы.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="e6c3f-152">Вызыватели, которые не работают в качестве Windows службы, не должны устанавливать этот флаг; Вызыватели, работающие в качестве службы, должны установить этот флаг.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="e6c3f-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="e6c3f-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="e6c3f-154">MAPILogonEx должен отображать диалоговое окно конфигурации для каждой службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="e6c3f-155">Диалоговые окна отображаются после того, как был выбран профиль, но перед входом в систему любой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="e6c3f-156">Общий диалоговое окно MAPI для logon также содержит чековое поле, которое запрашивает ту же операцию.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="e6c3f-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="e6c3f-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="e6c3f-158">Логон должен сбой, если он заблокирован более чем на несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="e6c3f-159">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e6c3f-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e6c3f-160">Переданные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="e6c3f-161">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="e6c3f-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="e6c3f-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="e6c3f-163">Подсистема обмена сообщениями должна заменить имя профиля профиля по умолчанию для _параметра lpszProfileName._</span><span class="sxs-lookup"><span data-stu-id="e6c3f-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="e6c3f-164">Флаг MAPI_EXPLICIT_PROFILE, если  _lpszProfileName_ не является NULL или пустым.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="e6c3f-165">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="e6c3f-165">_lppSession_</span></span>
  
> <span data-ttu-id="e6c3f-166">[вышел] Указатель на указатель на интерфейс сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6c3f-167">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6c3f-167">Return value</span></span>

<span data-ttu-id="e6c3f-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6c3f-168">S_OK</span></span> 
  
> <span data-ttu-id="e6c3f-169">Логотип удалось.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-169">The logon succeeded.</span></span>
    
<span data-ttu-id="e6c3f-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="e6c3f-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="e6c3f-171">Логотип был неудачным либо из-за того, что один или несколько параметров MAPILogonEx были недействительны, либо из-за того, что было открыто слишком много сеансов.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="e6c3f-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e6c3f-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="e6c3f-173">MAPI сериализует все логотипы через мутекс.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="e6c3f-174">Это возвращается, если MAPI_TIMEOUT_SHORT был установлен флаг и другой поток удерживает mutex.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="e6c3f-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="e6c3f-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="e6c3f-176">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e6c3f-177">Примечания</span><span class="sxs-lookup"><span data-stu-id="e6c3f-177">Remarks</span></span>

<span data-ttu-id="e6c3f-178">Клиентские приложения MAPI называют функцию MAPILogonEx для входа в сеанс с системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="e6c3f-179">Все строки, которые передаются и возвращаются на вызовы MAPI и обратно, не прекращаются и должны быть указаны в текущем наборе символов или на странице кода операционной системы вызываемого клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="e6c3f-180">Параметр  _lpszProfileName_ игнорируется, если существует существующая предыдущая сессия, называемая MapiLogonEx с набором флага MAPI_ALLOW_OTHERS и если флаг MAPI_NEW_SESSION не установлен.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="e6c3f-181">Если параметр  _lpszProfileName_ является NULL или указывает на пустую строку, а параметр  _flFlags_ включает флаг MAPI_LOGON_UI, функция MAPILogonEx создает диалоговое окно с пустым полем для имени профиля.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="e6c3f-182">При входе в определенный профиль клиент должен передать флаг MAPI_NEW_SESSION в MAPILogonEx в дополнение к имени профиля.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="e6c3f-183">В противном случае, если другой клиент создал общий сеанс, войдя в MAPI_ALLOW_OTHERS, клиент будет вошел в общий сеанс, а не в запрашиваемом профиле.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="e6c3f-184">Флаг MAPI_EXPLICIT_PROFILE не вызывает использования имени профиля по умолчанию, если  _lpszProfileName_ является NULL или пуст, если MAPI_USE_DEFAULT флаг также присутствует.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="e6c3f-185">Флаг MAPI_NO_MAIL имеет несколько эффектов, которые вызывают следующее при не использовании шпалер MAPI:</span><span class="sxs-lookup"><span data-stu-id="e6c3f-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="e6c3f-186">Во время этого сеанса шпалер MAPI не может отправлять или отправлять сообщения.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="e6c3f-187">Отправлять и доставлять сообщения могут только тесно скрепив магазины и поставщики транспорта.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="e6c3f-188">Серверные магазины по-прежнему могут отправлять или доставлять сообщения.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="e6c3f-189">Сообщения, отправленные или доставленные в хранилищах на сервере, не обрабатываются поставщиками крючков.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="e6c3f-190">Параметры переноса для каждого сообщения и каждого получателя недоступны.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="e6c3f-191">В таблице состояния не содержатся записи для поставщиков транспорта, а любые функции транспорта, зависящие от объектов состояния (например, конфигурации), недоступны.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="e6c3f-192">Строка spooler сообщения в таблице состояния содержит значение STATUS_FAILURE.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="e6c3f-193">Разрешены логотипы с копией, но эти логотипы не приводят к тому, что предыдущий логотип получает обновления объектов состояния.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="e6c3f-194">Служба всегда должна войти в систему с MAPI_NO_MAIL флагом.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e6c3f-195">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e6c3f-195">MFCMAPI reference</span></span>

<span data-ttu-id="e6c3f-196">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e6c3f-197">**Файл**</span><span class="sxs-lookup"><span data-stu-id="e6c3f-197">**File**</span></span>|<span data-ttu-id="e6c3f-198">**Функция**</span><span class="sxs-lookup"><span data-stu-id="e6c3f-198">**Function**</span></span>|<span data-ttu-id="e6c3f-199">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="e6c3f-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e6c3f-200">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="e6c3f-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="e6c3f-201">CMapiObjects::MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="e6c3f-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="e6c3f-202">MFCMAPI использует метод MAPILogonEx для входа в MAPI.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6c3f-203">См. также</span><span class="sxs-lookup"><span data-stu-id="e6c3f-203">See also</span></span>



[<span data-ttu-id="e6c3f-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="e6c3f-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="e6c3f-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="e6c3f-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="e6c3f-206">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="e6c3f-206">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

