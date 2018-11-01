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
ms.openlocfilehash: db76dfec27100a22785082580da70ecc2c10fc45
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579986"
---
# <a name="mapilogonex"></a><span data-ttu-id="1713c-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="1713c-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="1713c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1713c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1713c-105">Журналы клиентского приложения на сеанс с системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="1713c-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1713c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1713c-106">Header file:</span></span>  <br/> |<span data-ttu-id="1713c-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="1713c-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="1713c-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="1713c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1713c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1713c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1713c-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="1713c-110">Called by:</span></span>  <br/> |<span data-ttu-id="1713c-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="1713c-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="1713c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="1713c-112">Parameters</span></span>

 <span data-ttu-id="1713c-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1713c-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="1713c-114">[in] Дескриптор окна, к которому модальное диалоговое окно входа в систему.</span><span class="sxs-lookup"><span data-stu-id="1713c-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="1713c-115">Если появится диалоговое окно не во время вызова, параметр _ulUIParam_ игнорируется.</span><span class="sxs-lookup"><span data-stu-id="1713c-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="1713c-116">Этот параметр может быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1713c-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="1713c-117">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="1713c-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="1713c-118">[in] Указатель на строку, содержащую имя профиля, который будет использоваться при входе в систему.</span><span class="sxs-lookup"><span data-stu-id="1713c-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="1713c-119">Эта строка ограничена 64 символов.</span><span class="sxs-lookup"><span data-stu-id="1713c-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="1713c-120">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="1713c-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="1713c-121">[in] Указатель на строку, содержащую пароль профиля.</span><span class="sxs-lookup"><span data-stu-id="1713c-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="1713c-122">Параметр _lpszPassword_ должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="1713c-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="1713c-123">_flFlags_</span><span class="sxs-lookup"><span data-stu-id="1713c-123">_flFlags_</span></span>
  
> <span data-ttu-id="1713c-124">[in] Битовая маска флаги, используемые для управления, как выполнять вход в систему.</span><span class="sxs-lookup"><span data-stu-id="1713c-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="1713c-125">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="1713c-125">The following flags can be set:</span></span>
    
<span data-ttu-id="1713c-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="1713c-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="1713c-127">Совместный сеанс должно быть возвращено, что позволяет более поздней версии клиентов для получения сеанса не вводя учетные данные любого пользователя.</span><span class="sxs-lookup"><span data-stu-id="1713c-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="1713c-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="1713c-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="1713c-129">Вход в сеанс и выполнять любые операции в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="1713c-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="1713c-130">В целом если клиент планирует обработки в фоновом потоке, или в отдельном процессе, таким образом, чтобы выделялся основной поток, его вызова с флагом MAPI_BG_SESSION.</span><span class="sxs-lookup"><span data-stu-id="1713c-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="1713c-131">Клиентское приложение, например механизм индексирования или открытие личных папок файлов (PST) для фона тип доступа приведены некоторые примеры того, где можно использовать MAPI_BG_SESSION. MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="1713c-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="1713c-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="1713c-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="1713c-133">Профиль по умолчанию не должен использоваться и должны должен предоставить в профиль пользователя.</span><span class="sxs-lookup"><span data-stu-id="1713c-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="1713c-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="1713c-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="1713c-135">Выполните вход с помощью расширенных возможностей.</span><span class="sxs-lookup"><span data-stu-id="1713c-135">Log on with extended capabilities.</span></span> <span data-ttu-id="1713c-136">Этот флаг всегда должно иметь значение.</span><span class="sxs-lookup"><span data-stu-id="1713c-136">This flag should always be set.</span></span>
    
<span data-ttu-id="1713c-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="1713c-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="1713c-138">Предпринята попытка следует загрузить все сообщения пользователя перед возвращением.</span><span class="sxs-lookup"><span data-stu-id="1713c-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="1713c-139">Если флаг MAPI_FORCE_DOWNLOAD не установлен, сообщения можно загрузить в фоновом режиме после обращения к MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="1713c-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="1713c-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="1713c-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="1713c-141">Диалоговое окно должно отображаться для запроса пользователя для входа в систему сведения при необходимости.</span><span class="sxs-lookup"><span data-stu-id="1713c-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="1713c-142">Когда флаг MAPI_LOGON_UI не установлен, вызывающего клиента не отображает диалоговое окно входа в систему и возвращает ошибку, если пользователь не вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="1713c-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="1713c-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="1713c-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="1713c-144">Предпринята попытка следует создать новый сеанс MAPI вместо приобретение совместный сеанс.</span><span class="sxs-lookup"><span data-stu-id="1713c-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="1713c-145">Если флаг MAPI_NEW_SESSION не установлен, MAPILogonEx использует существующий совместный сеанс даже в том случае, если параметр _lpszprofileName_ не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="1713c-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="1713c-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="1713c-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="1713c-147">MAPI не сообщает о диспетчер очереди MAPI существования сеанса.</span><span class="sxs-lookup"><span data-stu-id="1713c-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="1713c-148">Результатом является, что сообщения не может быть отправку и получение в сеансе, за исключением того, через тесно связанных хранения и передачи пары.</span><span class="sxs-lookup"><span data-stu-id="1713c-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="1713c-149">Вызывающего клиента задает этот флаг, если она используется в качестве агента, если необходимо выполнить работу конфигурации, или если клиент просматривает хранилищ доступных сообщений.</span><span class="sxs-lookup"><span data-stu-id="1713c-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="1713c-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="1713c-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="1713c-151">Звонящий выполняется как служба Windows.</span><span class="sxs-lookup"><span data-stu-id="1713c-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="1713c-152">Вызывающие объекты, которые не выполняется как служба Windows не следует устанавливать этот флаг; вызывающие объекты, на которых выполняется как служба необходимо установить этот флаг.</span><span class="sxs-lookup"><span data-stu-id="1713c-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="1713c-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="1713c-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="1713c-154">MAPILogonEx должны отображать диалоговое окно настройки для каждой службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="1713c-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="1713c-155">Диалоговые окна отображаются после решила профиля, но до любых сообщений о службе вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="1713c-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="1713c-156">MAPI обычное диалоговое окно для входа в систему также содержит флажок, для которого запрашивается той же операции.</span><span class="sxs-lookup"><span data-stu-id="1713c-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="1713c-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="1713c-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="1713c-158">Вход в систему не выполняется, если заблокировано на несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="1713c-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="1713c-159">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1713c-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1713c-160">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="1713c-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="1713c-161">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="1713c-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="1713c-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="1713c-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="1713c-163">Подсистема обмена сообщениями необходимо заменить имя профиля по умолчанию для параметра _lpszProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="1713c-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="1713c-164">Флаг MAPI_EXPLICIT_PROFILE используется только _lpszProfileName_ имеет значение NULL или пуст.</span><span class="sxs-lookup"><span data-stu-id="1713c-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="1713c-165">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="1713c-165">_lppSession_</span></span>
  
> <span data-ttu-id="1713c-166">[out] Указатель на указатель на интерфейс сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="1713c-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1713c-167">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1713c-167">Return value</span></span>

<span data-ttu-id="1713c-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="1713c-168">S_OK</span></span> 
  
> <span data-ttu-id="1713c-169">Вход в систему успешно завершен.</span><span class="sxs-lookup"><span data-stu-id="1713c-169">The logon succeeded.</span></span>
    
<span data-ttu-id="1713c-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="1713c-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="1713c-171">Вход в систему не удалось выполнить, так как один или несколько параметров, чтобы MAPILogonEx недопустимы или из-за слишком большого числа сеансов open уже.</span><span class="sxs-lookup"><span data-stu-id="1713c-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="1713c-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="1713c-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="1713c-173">MAPI выполняет сериализацию всех имен входа через семафора.</span><span class="sxs-lookup"><span data-stu-id="1713c-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="1713c-174">Возвращается, если был установлен флажок MAPI_TIMEOUT_SHORT и другой поток проведенных семафора.</span><span class="sxs-lookup"><span data-stu-id="1713c-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="1713c-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="1713c-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="1713c-176">Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="1713c-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1713c-177">Замечания</span><span class="sxs-lookup"><span data-stu-id="1713c-177">Remarks</span></span>

<span data-ttu-id="1713c-178">Клиентские приложения MAPI вызовите функцию MAPILogonEx войти в сеанс с системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="1713c-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="1713c-179">Все строки, переданного и возвращаются в и из вызовов MAPI с символом null и должно быть указано в текущий набор символов или кодовая страница вызывающего клиента или поставщика операционной системы.</span><span class="sxs-lookup"><span data-stu-id="1713c-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="1713c-180">Параметр _lpszProfileName_ игнорируется, если имеется существующий предыдущего сеанса, который называется MapiLogonEx с установленным флагом MAPI_ALLOW_OTHERS и флаг MAPI_NEW_SESSION не установлен.</span><span class="sxs-lookup"><span data-stu-id="1713c-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="1713c-181">Если параметр _lpszProfileName_ имеет значение NULL или указывает на пустую строку, а параметр _flFlags_ включает флаг MAPI_LOGON_UI, функция MAPILogonEx создает диалоговое окно входа в систему с пустым полем для имени профиля.</span><span class="sxs-lookup"><span data-stu-id="1713c-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="1713c-182">При входе в определенный профиль, клиент должен передать флаг MAPI_NEW_SESSION в MAPILogonEx в дополнение к имени профиля.</span><span class="sxs-lookup"><span data-stu-id="1713c-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="1713c-183">В противном случае — если другого клиентского соединения, войдите в систему с MAPI_ALLOW_OTHERS сеанс клиента будет войти в сеанс с общим доступом вместо к профилю запрошено.</span><span class="sxs-lookup"><span data-stu-id="1713c-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="1713c-184">Флаг MAPI_EXPLICIT_PROFILE не привести к имени профиля по умолчанию для использования при _lpszProfileName_ имеет значение NULL или пустая, если не указан также флаг MAPI_USE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="1713c-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="1713c-185">Флаг MAPI_NO_MAIL имеет несколько эффекты, которые не используется диспетчер очереди MAPI привести к следующему:</span><span class="sxs-lookup"><span data-stu-id="1713c-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="1713c-186">Сообщения не могут отправленных или диспетчер очереди MAPI, предоставляемых во время данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="1713c-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="1713c-187">Только тесно связанных поставщиков хранилища и транспорта можно отправлять и доставлять сообщения.</span><span class="sxs-lookup"><span data-stu-id="1713c-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="1713c-188">Сервер на основе хранилища по-прежнему могут отправить или доставлять сообщения.</span><span class="sxs-lookup"><span data-stu-id="1713c-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="1713c-189">Сообщения, отправленные или доставки с сервера на основе хранилища не обрабатываются все поставщики обработчик.</span><span class="sxs-lookup"><span data-stu-id="1713c-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="1713c-190">Параметры каждого сообщения и каждого получателя для транспортировки недоступны.</span><span class="sxs-lookup"><span data-stu-id="1713c-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="1713c-191">В таблице состояния не содержит записи для поставщиков транспорта и функциональные возможности транспорта зависит от состояния объекты (например, конфигурации) недоступен.</span><span class="sxs-lookup"><span data-stu-id="1713c-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="1713c-192">Строка очереди сообщений в таблице состояния содержит значение STATUS_FAILURE.</span><span class="sxs-lookup"><span data-stu-id="1713c-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="1713c-193">Разрешены пополняется очередь входов в систему, но эти входы в систему, не приводят к предыдущей входа на получение обновлений состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="1713c-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="1713c-194">Службы всегда должны войти в систему с использованием флага MAPI_NO_MAIL.</span><span class="sxs-lookup"><span data-stu-id="1713c-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1713c-195">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1713c-195">MFCMAPI reference</span></span>

<span data-ttu-id="1713c-196">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="1713c-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1713c-197">**Файл**</span><span class="sxs-lookup"><span data-stu-id="1713c-197">**File**</span></span>|<span data-ttu-id="1713c-198">**Функция**</span><span class="sxs-lookup"><span data-stu-id="1713c-198">**Function**</span></span>|<span data-ttu-id="1713c-199">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="1713c-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1713c-200">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="1713c-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="1713c-201">CMapiObjects::MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="1713c-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="1713c-202">Mfcmapi (en) использует метод MAPILogonEx войдите в систему MAPI.</span><span class="sxs-lookup"><span data-stu-id="1713c-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1713c-203">См. также</span><span class="sxs-lookup"><span data-stu-id="1713c-203">See also</span></span>



[<span data-ttu-id="1713c-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="1713c-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="1713c-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="1713c-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="1713c-206">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="1713c-206">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

