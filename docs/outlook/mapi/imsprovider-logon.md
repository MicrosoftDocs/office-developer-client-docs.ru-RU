---
title: IMSProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Logon
api_type:
- COM
ms.assetid: 890d9cbe-3570-4cf0-aeae-667c0e5ba181
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: b89c8129f68852bdd243a7f984497ab312aa2551
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809456"
---
# <a name="imsproviderlogon"></a>IMSProvider::Logon

  
  
**Применимо к**: Outlook 
  
Журналы MAPI на один экземпляр поставщика хранилища сообщений.
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG FAR * lpcbSpoolSecurity,
  LPBYTE FAR * lppbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a>Parameters

 _lpMAPISup_
  
> [in] Указатель на текущий MAPI поддержку объектов хранилища сообщений.
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна из диалоговых окон и windows отображает этот метод. 
    
 _lpszProfileName_
  
> [in] Указатель на строку, содержащую имя профиля, используется для входа в систему поставщика хранилища. Эта строка может отображаются в диалоговых окнах, записывается в файл журнала или просто игнорируются. Он должен быть в формате Юникод, если флаг MAPI_UNICODE установлен в параметре _ulFlags_ . 
    
 _cbEntryID_
  
> [in] Размер в байтах, идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи для хранилища сообщений. Передача **значения null** в _lpEntryID_ указывает, что хранилище сообщений еще не был выбран и диалоговых окон, которые позволяют пользователю выбрать хранилище сообщений могут быть представлены. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как выполняется вход в систему. Можно задать следующие флажки:
    
MAPI_DEFERRED_ERRORS 
  
> Разрешено для успешного выполнения даже в том случае, если базовый объект недоступен для вызова реализации. Если объект недоступен, следующий вызов объекта может вызвать ошибку.
    
MAPI_UNICODE 
  
> Строки переданное хранятся в формате Юникод. Если MAPI_UNICODE не задано, они в формате ANSI.
    
MDB_NO_DIALOG 
  
> Не отображать диалоговые окна входа в систему. Если этот флаг установлен, возвращается значение ошибка MAPI_E_LOGON_FAILED, если вход в систему не удалось. Если этот флаг не установлен, поставщик хранения сообщений можно запрашивать пользователя в нужное имя или пароль, вставьте диск или выполнить другие действия, необходимые для установления подключения к хранилищу.
    
MDB_NO_MAIL 
  
> Хранилище сообщений не должна использоваться для отправке или получении почты. Флаг сигналы MAPI не следует уведомить диспетчер очереди MAPI открыта, что хранилища. Если этот флаг установлен, и хранилища сообщений тесно связан с поставщиком транспорта, поставщик вызовите метод [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) не требуется. 
    
MDB_TEMPORARY 
  
> Журналы для хранилища, чтобы сведения можно получить программным путем из раздела профиля без использование диалоговых окон. Этот флаг указывает MAPI, что хранилище не для добавления к таблице хранилища сообщений и, что хранилище не может принимать постоянной. Если установлен этот флаг, вызовите метод [IMAPISupport::ModifyProfile](imapisupport-modifyprofile.md) поставщиков хранилища сообщений не требуется. 
    
MDB_WRITE 
  
> Запросы на разрешение чтения и записи.
    
 _lpInterface_
  
> [in] Указатель на интерфейс идентификатор (ИД интерфейса) для хранилища сообщений для входа в систему. Передача **значения null** указывает, что возвращается интерфейс MAPI для хранилища сообщений ( [IMsgStore](imsgstoreimapiprop.md)). Параметр _lpInterface_ можно также назначается идентификатор соответствующий интерфейс для хранилища сообщений (например, IID_IUnknown или IID_IMAPIProp). 
    
 _lpcbSpoolSecurity_
  
> [out] Указатель на переменную, в котором поставщик хранения возвращает размер, в байтах, проверки данных с помощью параметра _lppbSpoolSecurity_ . 
    
 _lppbSpoolSecurity_
  
> [out] Указатель на указатель на возвращаемый проверки данных. Эти данные проверки предоставляется, метод [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) можно войдите диспетчер очереди MAPI на том же хранилище в качестве поставщика хранилища сообщений. 
    
 _lppMAPIError_
  
> [out] Указатель на указатель на возвращенный [MAPIERROR](mapierror.md) структуры, если они существуют, который содержит сведения о версии, компонент и контекста для ошибки. Параметр _lppMAPIError_ может быть присвоено **значение null,** Если нет **MAPIERROR** структуры для возврата. 
    
 _lppMSLogon_
  
> [out] Указатель на указатель на сообщение хранить объект входа в систему для MAPI для входа в систему.
    
 _lppMDB_
  
> [out] Указатель на указатель на сообщение хранилища объект для очереди MAPI и клиентскими приложениями для входа в систему.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_FAILONEPROVIDER 
  
> Этот поставщик не может войти, но эта ошибка не следует отключить службу. 
    
MAPI_E_LOGON_FAILED 
  
> Не удается установить сеанса входа в систему.
    
MAPI_E_UNCONFIGURED 
  
> Профиль не содержит достаточно сведений для входа в систему для выполнения. При возвращении это значение MAPI вызывает функцию точки входа службы сообщений поставщика хранилища сообщений.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне. 
    
MAPI_E_UNKNOWN_CPID 
  
> Сервер не настроен для поддержки кодовой страницы клиента.
    
MAPI_E_UNKNOWN_LCID 
  
> Сервер не настроен для поддержки сведения о языковом стандарте клиента.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов завершился успешно, но поставщика хранилища сообщений имеет доступные сведения об ошибке. При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md). Чтобы получить сведения об ошибке от поставщика, вызовите метод [IMAPISession::GetLastError](imapisession-getlasterror.md) . 
    
## <a name="remarks"></a>Замечания

MAPI вызывает метод **IMSProvider::Logon** для выполнения большинства обработку, необходимую для получения доступа к хранилищу сообщений. Поставщики хранилища сообщений проверки любого пользователя учетные данные для доступа к конкретной хранилища и возвращает объект хранилища сообщений с помощью параметра _lppMDB_ , который может входить очереди и клиентских приложений MAPI. 
  
В дополнение к объекта хранилища возвращенные сообщения для клиентов и использования диспетчера очереди MAPI поставщик также возвращает объект сообщения хранилища входа в систему для MAPI для использования в управлении открыт хранилища. Объект вход в систему хранения сообщений и объектов хранилища сообщений должны быть тесно связаны внутри поставщика хранилища сообщений, каждый влияют на другой. Использование объекта хранилища и объект вход в систему должны совпадать; Таким образом, что объекты действовать как если бы они были одного объекта, который предоставляет два из них следует однозначного соответствия между объект вход в систему и объект хранилища. Два объекта следует также создавать вместе и освобожденное друг с другом. 
  
Объект поддержки MAPI, созданные MAPI и передан поставщика с помощью параметра _lpMAPISup_ предоставляет доступ к функциям в MAPI, которому требуется поставщик. К ним относятся функции, которые сохранения и извлечения данных профиля, доступ к адресной книги и т.д. Указатель _lpMAPISup_ может быть различным для каждого хранилища, который открывается. Во время обработки вызывает для хранилища сообщений после входа в систему, поставщик хранения следует использовать переменную _lpMAPISup_ , характерные для этого хранилища. Для вызова любого **входа в систему** , которая открывает хранилища сообщений и успешно создает объект входа хранилища сообщений поставщик должен быть сохранен указателя на объект поддержки MAPI в объекте входа хранилища и необходимо вызвать метод [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) для добавления ссылки для объект поддержки. 
  
Параметр _ulUIParam_ следует использовать, если поставщик отображаются диалоговые окна во время вызова **входа в систему** . Тем не менее диалоговые окна не должны быть представлены, если _ulFlags_ содержит флаг MDB_NO_DIALOG. Если нужно вызвать пользовательского интерфейса, но не позволяет _ulFlags_ или по другой причине не может отображаться пользовательского интерфейса, поставщик должен возвращать MAPI_E_LOGON_FAILED. Если открывает диалоговое окно **входа в систему** и пользователь отменил вход в систему, как правило, нажав кнопку **Отмена** диалоговое окно "", поставщик должен возвращать MAPI_E_USER_CANCEL. 
  
Параметр _lpEntryID_ может иметь **значение null,** или выберите команду развернуть хранилища запись идентификатора, сохранить это сообщение ранее созданный. Если _lpEntryID_ указывает идентификатор зоны запись, этот идентификатор записи могут поступать из одного из нескольких местах: 
  
- Это может быть идентификатор записи, которая поставщика хранилища оболочку и ранее был создан в разделе профиль как свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
- Это может быть идентификатор входа, который поставщик оболочку и ранее возвращенный вызывающего клиента как свойство **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)). 
    
- Это может быть идентификатор входа, который поставщик ранее оболочку и возвращается для вызывающего клиента как свойство **PR_ENTRYID** объекта хранилища сообщений. 
    
В обоих случаях возможно, на другом компьютере, используемый в настоящее время создания идентификатор записи.
  
При _lpEntryID_ не равно **null**, он должен содержать все сведения, необходимые для идентификации и найдите хранилище сообщений. Эти сведения могут включать имена многопользовательской сетевой, номера телефонов, имена учетных записей пользователей и т. д. Если не удается установить связь в хранилище с помощью данных в идентификатор записи, поставщик хранения должны отображать диалоговое окно, которое позволяет пользователю выбрать хранилище для открытия. Диалоговое окно может потребоваться, например, если была переименована сервера, имя учетной записи был изменен или части сети, недоступны.
  
Когда _lpEntryID_ имеет **значение null**, используйте хранение сообщений еще не был выбран. Поставщик может по-прежнему доступа к хранилищу без отображения диалогового окна, если он поддерживает дополнительные методы для указания в хранилище. Например поставщик можно проверить его файла инициализации или, который можно найти дополнительные свойства, которые находятся в разделе его или ее сообщения службы профилей в конфигурации.
  
Если поставщик обнаруживает, что все, что не является необходимой информации в профиле, он должен возвращать MAPI_E_UNCONFIGURED. MAPI затем вызовет функцию точки входа службы сообщений поставщика для включения пользователя для выбора хранилища или даже для его создания и введите имя учетной записи и пароль, как требуется. MAPI автоматически создает новый раздел профиля для нового хранилища; в этом разделе новый профиль может быть временное или постоянное, в зависимости от того, как она была добавлена. Если поставщик хранения вызывает метод **IMAPISupport::ModifyProfile** , новый раздел профиль становится постоянной и хранилище добавляется в список хранилищ сообщений, возвращенных методом [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
Параметр _lpInterface_ указывает ИД интерфейса интерфейса, необходимые для объекта открываемые хранилища. Передача **значения null** в _lpInterface_ указывает, что интерфейс хранилища сообщений MAPI, **IMsgStore**обязательным. Также с передачей объекта хранилища сообщений, IID_IMsgStore, указывает, что **IMsgStore** является обязательным. Если IID_IUnknown передается в _lpInterface_, поставщик должен открыть хранилище с помощью любой интерфейс производным от [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) лучше всего подходит для поставщика (еще раз, обычно это **IMsgStore**). При передаче IID_IUnknown, вызывающий реализации использует метод [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) для выбора интерфейс после успешного завершения операции открытия хранилища. 
  
Вызов **IMSProvider::Logon** возвращает достаточно данных, например путь для хранения и учетные данные для доступа к хранилища, чтобы разрешить диспетчер очереди MAPI, войдите в систему из одного хранилища, который выполняет поставщика хранилища без предоставления диалоговое окно. Параметры _lpcbSpoolSecurity_ и _lppbSpoolSecurity_ используются для возврата эти сведения. Поставщик выделения памяти для этих данных, передав указатель на буфер в параметре _lpfAllocateBuffer_ функции [MSProviderInit](msproviderinit.md) ; Поставщик устанавливает размер буфера в _lpcbSpoolSecurity_. 
  
MAPI освобождает буфер при необходимости. Если диспетчер очереди MAPI входа в хранилище может быть выполнена на основании сведений в разделе профиля сам по себе он, поставщик может возвращать значение null, в _lppbSpoolSecurity_ и 0 для размер сведения в _lpcbSpoolSecurity_. Выполняется вход очереди MAPI в ходе процесса различных чем входа хранения; Поскольку буфер, содержащий переданные данные получает скопировать между процессами, может оказаться в памяти в одном месте для процесса очереди MAPI как для процесс поставщика хранилища. Таким образом поставщик не следует поместить адреса в этот буфер. Дополнительные сведения о входе в очереди MAPI [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) см. 
  
Большинство поставщиков хранилища используйте метод [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) объекта поддержки, переданной в параметре _lpMAPISup_ для сохранения и извлечения учетных данных и параметры. **OpenProfileSection** включает поставщика хранилища для сохранения дополнительных произвольных сведений в разделе профилей и связать его с определенного ресурса. Например поставщик хранения можно сохранить имя учетной записи пользователя и пароль, связанный с ресурсом и любые пути или другие сведения, необходимые для доступа к этому ресурсу. 
  
Свойства с идентификаторами свойство 0x6600 через 0x67FF — это свойства безопасности для поставщика для собственного использования для хранения личных данных в разделах профилей. Дополнительные сведения об использовании свойств в раздел объекты профиля можно [IProfSect: IMAPIProp](iprofsectimapiprop.md) метод. 
  
В дополнение к любой личных данных в свойства с идентификаторами 0x6600 через 0x67FF поставщика хранилища предоставьте сведения для свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) в разделе его профиля. Его следует поместить в **PR_DISPLAY_NAME** отображаемое имя поставщика хранилища, идентифицирующая строка (например, «личный банка данных Microsoft»), который отображается для пользователей, чтобы они отличать этого хранилища сообщений от других пользователей они могут иметь доступ к Кому. **PR_DISPLAY_NAME** часто содержит имя сервера, имя учетной записи пользователя или путь. 
  
Некоторые свойства раздела профиля отображаются в таблице хранилища сообщений; другие пользователи являются видимыми во время установки, установки и настройки подсистемы MAPI. Поставщик обычно сведения для обоих этих отображаемых свойств новый раздел профиля, который еще не содержит сохраненные учетные данные или конфиденциальных сведений, а при обнаружении был изменен, что сведения о свойствах. Дополнительные сведения о разделах профиля можно [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md).
  
После успешного входа на пользователя и перед возвращением MAPI, поставщик хранения следует создать массив свойств в строке состояния для ресурса и вызовите метод [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . 
  
 Вызовы **входа в систему** , откройте хранилищ сообщений, которые уже открыты для текущего сеанса MAPI пропустить большую часть обработки описанных выше. Эти вызовы не Создание строк состояния, возвращающие объекты входа хранилища сообщений, вызовите **метод AddRef** для объектов поддержки MAPI или возвращаются данные для входа в систему очереди MAPI. Эти вызовы возвращает значение S_OK и возвращает объект хранилища сообщений со запрашиваемого интерфейса. 
  
Чтобы обнаружить такие вызовы, поставщик необходимо поддерживать списка в объекте поставщика хранилища сообщений хранилищ уже открытой для данного объекта поставщика. При обработке вызовов **входа в систему** , поставщик должен сканировать этот список open хранилищ и определить, является ли хранилища, которое требуется выполнить вход на уже open. Если он установлен, учетные данные пользователя необходимо проверить, и следует избегать отображаемое диалоговое окно, если это возможно. Если необходимо отображать диалоговые окна, поставщик должен проверить, возвращенных данных, чтобы увидеть, был ли хранилище открыт еще раз. Кроме того, поставщик должен проверить для повторяющихся отверстия, с помощью _lpEntryID_ в начале вызова **входа в систему** обработки. 
  
Стандартный обработки для **входа в систему** вызов, который осуществляет доступ к open хранилища выглядит следующим образом: 
  
1. Поставщик хранения вызывает **AddRef** для существующего объекта хранилища, если запрошен нового интерфейса совпадает с интерфейс для имеющееся хранилище. В противном случае вызывает **QueryInterface** для получения нового интерфейса. Если хранилище не поддерживает новый интерфейс, поставщик должен возвращать значение ошибки MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Поставщик возвращает указатель на требуемый интерфейс существующий объект хранилища в _lppMDB_.
    
3. Поставщик возвращает **значение null,** в _lppMSLogon_.
    
4. Поставщик не следует открывать профиля для поддержки объекта, переданного в вызов. Кроме того его следует не зарегистрировать уникальный идентификатор поставщика, зарегистрируйте строки состояния и возврата диспетчер очереди MAPI данные входа в систему.
    
5. Поставщик не должны вызывать **метод AddRef** объекта поддержки, так как не требует указателя на объект. 
    
По возможности поставщиков должна вернуть соответствующие ошибки и предупреждение строк для **входа в систему** вызовов, поскольку это значительно облегчает нагрузку пользователей при определении, почему что-то не работает. Для возврата эти строки, поставщик задает элементы в структуре **MAPIERROR** . MAPI выполняет поиск, использует и освобождает структуры **MAPIERROR** , если он возвращается поставщиком. 
  
С помощью буфера, переданных в _lpfAllocateBuffer_ вызовов **MSProviderInit** следует выделить память для этой структуры **MAPIERROR** . Любая ошибка, содержащихся в структуре возвращенных строк следует в формате Юникод, если MAPI_UNICODE устанавливается на **Вход в систему** _ulFlags;_ в противном случае, они должны быть в формате ANSI символ настроены. 
  
Для большинства ошибок, возвращаемые **входа в систему**MAPI отключает службы сообщений, к которым принадлежит поставщика со сбоями. MAPI не будут вызывать любой поставщиков, относящихся к этим службам в течение времени жизни сеанса MAPI. С другой стороны при **входе в систему** возвращает значение ошибки MAPI_E_FAILONEPROVIDER из его входа в систему, MAPI не отключайте службы сообщений, к которой принадлежит поставщик. Если возникает ошибка, которая не гарантирует отключение всей службы в течение сеанса **входа в систему** должна вернуть MAPI_E_FAILONEPROVIDER. К примеру поставщик может возвращать Эта ошибка при не разрешает отображение пользовательского интерфейса и требуемые пароля недоступен. 
  
Если поставщик возвращает MAPI_E_UNCONFIGURED из его входа в систему, MAPI вызовите функцию запись службы поставщика сообщение и повторите вход в систему. MAPI передает MSG_SERVICE_CONFIGURE в качестве контекста для предоставления возможности для настройки службы. Если принято решение клиента разрешить пользовательского интерфейса при входе в систему, службу можно представить его свойств конфигурации, пользователь может ввести сведения о конфигурации.
  
## <a name="see-also"></a>См. также



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::ModifyProfile](imapisupport-modifyprofile.md)
  
[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
  
[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)
  
[IProfSect: IMAPIProp](iprofsectimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MSProviderInit](msproviderinit.md)
  
[IMSProvider: IUnknown](imsprovideriunknown.md)
