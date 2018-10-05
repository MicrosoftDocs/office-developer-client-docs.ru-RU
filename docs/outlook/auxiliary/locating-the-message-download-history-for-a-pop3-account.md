---
title: Поиск журнала скачивания сообщений для учетной записи POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: В этом разделе описывается, как почтового клиента можно получить доступ к свойству PidTagAttachDataBinary для получения журнала загрузки сообщений для учетной записи POP3.
ms.openlocfilehash: ae12a044098aa4f42e1c2e5936e82da3d7a128dd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399560"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a>Поиск журнала скачивания сообщений для учетной записи POP3

В этом разделе описывается, как почтового клиента можно получить доступ к свойству [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) для получения журнала загрузки сообщений для учетной записи POP3. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a>

## <a name="why-get-the-message-download-history"></a>Почему получить журнала загрузки сообщений?

Поставщик протокол POP (Post Office) для Outlook позволяет пользователям для получения и загрузки новых сообщений электронной почты для своих локальных устройств и впоследствии оставьте или удалять эти сообщения электронной почты на почтовом сервере. При почтового клиента проверяет наличие новых сообщений для загрузки, она должна быть возможность определения и загружать только новые сообщения для этой папки "Входящие". Почтовый клиент достигается первого с помощью команды UIDL (уникальный идентификатор со списком), который получает карта каждого сообщения, когда-либо было доставлено для этой папки "Входящие" с уникальным идентификатором (UID). Клиент получает журнала загрузки сообщений для сообщений, которые загружаются или удалены для папки "Входящие" на клиента. С помощью сообщения UID карты и журнал загрузки, клиент может затем определите сообщения, отсутствующих в журнал как новый и, следовательно, необходимо загрузить.
  
Чтобы получить журнала загрузки сообщений для папки "Входящие":
  
- Выполните действия, описанные в этом разделе, чтобы найти свойство **PidTagAttachDataBinary** , который содержит журнал в больших двоичных объектов (BLOB), исходя из определенных форматов. 
    
- Выполните [Анализ журнала загрузки сообщений для учетной записи POP3](parsing-the-message-download-history-for-a-pop3-account.md), который описывает, как выполнить синтаксический анализ этой больших двоичных ОБЪЕКТОВ для идентификации сообщений, которые загружаются или удалены для этой папки "Входящие".
    
## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a>Основные понятия, которые необходимо знать при поиске сообщения журнала загрузки

Журнал загрузки сообщений для папки «Входящие» хранится в двоичного свойства MAPI, **PidTagAttachDataBinary**на вложение скрытого сообщения в папке "Входящие". В таблице 1 приведены ресурсы, необходимые для журнала загрузки справки, вам понять, как найти сообщение концепции.
  
**Таблица 1. Основные понятия**

|**Название статьи**|**Описание**|
|:-----|:-----|
|[����� MAPI �������](https://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |MAPI позволяет клиентам почты для хранения сведений в скрытых папках и скрытые сообщения. Скрытые папки в связанной части папки MAPI и обычно содержат информацию, которая не отображается в, а не управлять пользователями. Клиенты решить, формат и содержимое для хранения в скрытых сообщениях в скрытых папках.  <br/> |
|[Сообщения MAPI](https://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |MAPI хранит сообщения, либо в стандартный поддерева IPM, который отображается для пользователей клиента, или за ее пределами поддерева и невидимы для пользователей. Сообщения, могут иметь дополнительные данные, хранящиеся в вложения, который может быть в виде файла, другое сообщение или объекта OLE. В случае журнала загрузки сообщений журнала хранится в свойстве сообщения, подключенный к другой скрытого сообщения.  <br/> |
|[Общие сведения о свойствах сообщений](https://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |Когда клиент сохраняет данные в сообщении, фактически хранит сведения в свойстве сообщения. MAPI поддерживает множество свойства — некоторые всегда существует и может быть установлен с клиентами, другие являются необязательными, и клиенты не могут ожидать от них недоступны или переместить на допустимые значения. Журнала загрузки сообщений хранится в свойстве **PidTagAttachDataBinary** вложения в скрытого сообщения.  <br/> |
|[Профили MAPI](https://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |Во время входа в сеансе почтового клиента выбирает профиль, который описывает поставщики и служб, которые будут использоваться. Профиль делится на разделы, содержащие свойства. В частности свойства [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) (**PR_PROFILE_NAME**) и [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) всегда существует. Клавиша поиска профиля уникальным во всех профилях и хранится в разделе профиля, который идентифицируется средством **MUID_PROFILE_INSTANCE** (которая определена в MAPIGUID. H). Используйте [IMAPISession::OpenProfileSection](https://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx) откройте раздел и использовать [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) для получения значения свойств.  <br/> |
|[Таблицы содержимого](https://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |Содержимое таблицы для своих папок, реализуемые поставщиками хранилища сообщений. Скрытые сообщения в связанных части папки поставщиков хранилища сообщений поддерживает связанного содержимого таблицы и клиентов можно использовать метод [IMAPIContainer::GetContentsTable](https://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx) возвращает указатель в таблице связанного содержимого.  <br/> |
|[Сведения об ограничениях](https://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [Типы ограничений](https://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [Создание ограничения](https://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [Пример кода ограничения](https://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |В MAPI клиенты могут использовать ограничения для фильтрации содержимого таблицы, для поиска строк, которые представляют сообщения, для которых задано значение определенного определенное свойство. Ограничения определяются с помощью структуры данных [SRestriction](https://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx) , которая может содержать объединение более специализированных структур ограничение. Метод [IMAPITable::FindRow](https://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx) применяет ограничение и отображает первой строки в таблице, которая соответствует условиям ограничение.  <br/> |
|[Сведения о регистрации хранилищ для индексирования](https://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |Используйте свойство [PidTagStoreProvider](https://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) (**PR_MDB_PROVIDER**) для проверки типа поставщика хранилища. К примеру для проверки, является ли хранилище хранилища Exchange, свойство **PidTagStoreProvider** должен возвращать значение, представленное константу **pbExchangeProviderPrimaryUserGuid**, определенный в edkmdb.h файл общедоступных заголовка.  <br/> |
   
## <a name="locating-the-appropriate-hidden-message-and-attachment"></a>Поиск соответствующих скрытого сообщения и вложения

Теперь, когда мы знаем, что в свойстве **PidTagAttachDataBinary** вложения в скрытого сообщения журнала загрузки сообщений для папки "Входящие", описанную процедуру, чтобы указать соответствующие вложение соответствующие скрытого сообщения состоит из следующих из следующих процедур. 
  
1. [Найдите соответствующие скрытого сообщения](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)
    
2. [Поиск соответствующих вложений скрытого сообщения](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)
    
3. [Доступ к свойству PidTagAttachDataBinary вложения сообщения](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a>

### <a name="find-the-appropriate-hidden-message"></a>Найдите соответствующие скрытого сообщения

1. Получите свойство [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) из профиля, в разделе профиля, указанного идентификатором **MUID_PROFILE_INSTANCE**.
    
2. Откройте связанное содержимое для папки "Входящие" путем вызова **IMAPIContainer::GetContentsTable**.
    
3. Создания ограничения на основе [PidTagConversationKey](https://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (**PR_CONVERSATION_KEY**), **PidTagSearchKey** (**PR_SEARCH_KEY**) и свойства [PidTagMessageClass](https://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) (**PR_MESSAGE_CLASS**) для получения таблицы, содержит все скрытые сообщения в связанное содержимое папки «Входящие». Ниже приведен пример ограничений, извлеченные из [поиска журнал UIDL POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx).
    
   ```cpp
      SRestriction rgRes[3]; 
      SPropValue rgProps[3]; 
      rgRes[0].rt = RES_AND; 
      rgRes[0].res.resAnd.cRes = 2; 
      rgRes[0].res.resAnd.lpRes = &amp;rgRes[1]; 
      rgRes[1].rt = RES_PROPERTY; 
      rgRes[1].res.resProperty.relop = RELOP_EQ; 
      rgRes[1].res.resProperty.ulPropTag = PR_CONVERSATION_KEY; 
      rgRes[1].res.resProperty.lpProp = &amp;rgProps[0]; 
      rgRes[2].rt = RES_PROPERTY; 
      rgRes[2].res.resProperty.relop = RELOP_EQ; 
      rgRes[2].res.resProperty.ulPropTag = PR_MESSAGE_CLASS; 
      rgRes[2].res.resProperty.lpProp = &amp;rgProps[1]; 
      rgProps[0].ulPropTag = PR_CONVERSATION_KEY; 
      rgProps[0].Value.bin = pVals[iSearchKey].Value.bin; // PR_SEARCH_KEY from the profile 
      rgProps[1].ulPropTag = PR_MESSAGE_CLASS; 
      rgProps[1].Value.LPSZ = (LPTSTR)"IPM.MessageManager";
   ```

4. В таблице поиск скрытого сообщения с помощью **IMAPITable::FindRow**.
    
5. Если не удается найти скрытого сообщения шаг 4, изменения ограничения на использование **PidTagSearchKey** (**PR_SEARCH_KEY**) вместо **PidTagConversationKey**, как показано ниже:
    
   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. Поиск скрытого сообщения, с помощью **IMAPITable::FindRow**. 
    
7. В случае сбоя шаг 6 изменения ограничения для использования [PidTagSubject](https://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**PR_SUBJECT**), равное следующее значение (показано ниже, с помощью `printf` стиля замену для краткости). 
    
   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. Поиск скрытого сообщения с помощью **IMAPITable::FindRow**.
    
9. При запуске Outlook 2010 или более поздней версии, используйте следующие значения для **PidTagProfileName** (**PR_PROFILE_NAME**) и **PidTagSearchKey** (**PR_SEARCH_KEY**), соответственно.
    
   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   Выполните шаги 3 – 8. Если это не удается найти сообщение, вернуться к исходной шаги 3 – 8.
    
10. Откройте скрытого сообщения, определенные в действии 4, 6 или 8.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a>Поиск соответствующих вложений скрытого сообщения

Так как скрытые сообщения может иметь более одного вложения, ищите соответствующие вложений в следующем порядке.
  
> [!NOTE]
> В этой процедуре используются повторно `printf` стиля замену для краткости. 

1. Найдите вложения, [PidTagAttachLongFilename](https://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) соответствует следующую строку, где `szEmailAddress` — это SMTP-адрес пользователя, как указано в профиле пользователя. . 
    
   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. Найдите вложения, [PidTagAttachFilename](https://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) (**PR_ATTACH_FILENAME**) соответствует «BlobPOP %s» `szEmailAddress`.
    
3. Найдите вложения, [PidTagDisplayName](https://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) (**PR_DISPLAY_NAME**) соответствует «BlobPOP %s» `szEmailAddress`.
    
4. Найдите вложения, **PidTagAttachFilename** (**PR_ATTACH_FILENAME**) соответствует «Blob%.8x» `dwAcctUID`, где `dwAcctUID` , поступающие из [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md). Метод [IOlkAccount::GetProp](iolkaccount-getprop.md) для доступа к свойству **PROP_ACCT_MINI_UID** . 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a>Доступ к свойству PidTagAttachDataBinary вложения сообщения

После нахождения соответствующего сообщения вложение скрытые сообщения, используйте **IMAPIProp::GetProps** для чтения свойство **PidTagAttachDataBinary** вложения. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a>

## <a name="next-steps"></a>Дальнейшие действия

В данном разделе узнали как найти журнала загрузки сообщений для папки "Входящие" почтового клиента протокола POP3. В разделе [синтаксический анализ журнала загрузки сообщений для учетной записи POP3](parsing-the-message-download-history-for-a-pop3-account.md) , чтобы узнать, как выполнить синтаксический анализ данного журнала для идентификации сообщений, которые загружаются или удалены для папки «Входящие». 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a>

## <a name="see-also"></a>См. также

- [Управление скачиванием сообщений для учетных записей POP3](managing-message-downloads-for-pop3-accounts.md)   
- [Анализ журнала скачивания сообщений для учетной записи POP3](parsing-the-message-download-history-for-a-pop3-account.md)
- [Поиск истории UIDL POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    

