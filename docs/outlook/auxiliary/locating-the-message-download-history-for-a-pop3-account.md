---
title: Поиск журнала скачивания сообщений для учетной записи POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: В этом разделе описывается, как почтовый клиент может получить доступ к свойству PidTagAttachDataBinary для получения истории скачивания сообщений для учетной записи POP3.
ms.openlocfilehash: ae12a044098aa4f42e1c2e5936e82da3d7a128dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321877"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a>Поиск журнала скачивания сообщений для учетной записи POP3

В этом разделе описывается, как почтовый клиент может получить доступ к свойству [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) для получения истории скачивания сообщений для учетной записи POP3. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a>

## <a name="why-get-the-message-download-history"></a>Зачем получать историю скачивания сообщений?

Поставщик протокола Office (POP) для Outlook позволяет пользователям извлекать и загружать новые сообщения электронной почты на локальном устройстве, а затем оставлять или удалять эти сообщения электронной почты на почтовом сервере. Когда почтовый клиент проверяет загрузку новых сообщений, он должен иметь возможность идентифицировать и скачивать только новые сообщения для этого почтового ящика. Почтовый клиент сначала использует команду UIDL (Unique ID Listing), которая получает карту каждого сообщения, которое когда-либо доставлялось в этот почтовый ящик уникальному идентификатору (UID). Клиент также получает историю скачивания сообщений для сообщений, которые были загружены или удалены для почтового ящика на этом клиенте. Используя карту UID сообщения и историю скачивания, клиент может идентифицировать те сообщения, которые отсутствуют в истории, как новые и, следовательно, должны быть загружены.
  
Чтобы получить историю скачивания сообщения для почтового ящика:
  
- Выполните действия в этом разделе, чтобы найти свойство **PidTagAttachDataBinary,** которое содержит историю в двоичном большом объекте (BLOB), который следует определенному формату. 
    
- Продолжить с помощью размыкания истории скачивания сообщений для учетной записи [POP3,](parsing-the-message-download-history-for-a-pop3-account.md)которая описывает, как размыть этот BLOB для определения сообщений, которые были загружены или удалены для этого почтового ящика.
    
## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a>Основные понятия, которые необходимо знать для размещения истории скачивания сообщений

История скачивания сообщений для почтового ящика хранится в двоичном свойстве MAPI **PidTagAttachDataBinary** на вложении скрытого сообщения в почтовом ящике. В таблице 1 показаны ресурсы для понятий, которые помогают понять, как найти историю скачивания сообщений.
  
**Таблица 1. Основные понятия**

|**Название статьи**|**Описание**|
|:-----|:-----|
|[Скрытые папки MAPI](https://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |MAPI позволяет почтовым клиентам хранить сведения в скрытых папках и скрытых сообщениях. Скрытые папки находятся в связанной части папок MAPI и обычно содержат сведения, которые не видны пользователям и которыми не управляют пользователи. Клиенты решают формат и содержимое для хранения скрытых сообщений в скрытых папках.  <br/> |
|[Сообщения MAPI](https://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |MAPI хранит сообщения в папках, как в стандартной подтрите IPM, которая видна пользователям клиента, так и за пределами подтрия и невидимой для пользователей. Сообщения могут иметь дополнительные данные, хранимые в вложении, которые могут быть в виде файла, другого сообщения или объекта OLE. В случае истории скачивания сообщений история хранится в свойстве сообщения, прикрепленного к другому скрытому сообщению.  <br/> |
|[Обзор свойств сообщений](https://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |Когда клиент хранит сведения в сообщении, он фактически сохраняет сведения в свойстве сообщения. MAPI поддерживает многие свойства: некоторые всегда существуют и могут быть установлены клиентами, другие необязательны, и клиенты не могут ожидать, что они будут доступны или заданная для допустимых значений. История скачивания сообщений хранится в **свойстве PidTagAttachDataBinary** вложения к скрытому сообщению.  <br/> |
|[Профили MAPI](https://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |Во время логотипа в сеансе почтовый клиент выбирает профиль, в который описываются используемые поставщики и службы. Профиль делится на разделы, содержащие свойства. В частности, свойства [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) **(PR_SEARCH_KEY)** и [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) **(PR_PROFILE_NAME)** всегда существуют. Ключ поиска профиля уникален среди всех профилей и хранится в разделе **профилей,** который определяется MUID_PROFILE_INSTANCE (который определяется в MAPIGUID. H). Чтобы открыть раздел, используйте [IMAPISession::OpenProfileSection](https://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx) и используйте [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) для получения значений свойств.  <br/> |
|[Таблицы контента](https://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |Поставщики магазинов сообщений реализуют таблицы контента для своих папок. Для скрытых сообщений в связанной части папки поставщики магазинов сообщений поддерживают связанные таблицы содержимого, а клиенты могут использовать метод [IMAPIContainer::GetContentsTable,](https://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx) чтобы вернуть указатель в связанную таблицу содержимого.  <br/> |
|[Об ограничениях](https://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [Типы ограничений](https://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [Создание ограничения](https://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [Пример кода ограничений](https://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |В MAPI клиенты могут использовать ограничения для фильтрации таблиц контента, для поиска строк, которые представляют сообщения, которые имеют определенное свойство, заданная определенному значению. Ограничения определяются с помощью [структуры данных SRestriction,](https://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx) которая может содержать объединение более специализированных структур ограничений. Метод [IMAPITable::FindRow](https://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx) применяет ограничение и извлекает первую строку в таблице, которая соответствует критериям ограничения.  <br/> |
|[О регистрации магазинов для индексации](https://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |Используйте [свойство PidTagStoreProvider](https://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) **(PR_MDB_PROVIDER)** для проверки типа поставщика магазина. Например, чтобы проверить, является ли магазин Exchange магазином, свойство **PidTagStoreProvider** должно возвращать значение, представленное постоянным **pbExchangeProviderPrimaryUserGuid,** которое определяется в файле общедоступных заголовок edkmdb.h.  <br/> |
   
## <a name="locating-the-appropriate-hidden-message-and-attachment"></a>Поиск соответствующего скрытого сообщения и вложения

Теперь, когда мы знаем, что история скачивания сообщений для почтового ящика находится в свойстве **PidTagAttachDataBinary** вложения к скрытому сообщению, процедура поиска соответствующего вложения соответствующего скрытого сообщения включает следующие процедуры: 
  
1. [Поиск соответствующего скрытого сообщения](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)
    
2. [Поиск соответствующего вложения скрытого сообщения](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)
    
3. [Доступ к свойству PidTagAttachDataBinary вложения сообщения](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a>

### <a name="find-the-appropriate-hidden-message"></a>Поиск соответствующего скрытого сообщения

1. Получите свойство [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) **(PR_SEARCH_KEY)** из профиля в разделе профиль, **заданном** MUID_PROFILE_INSTANCE .
    
2. Откройте связанное содержимое папки "Входящие", позвонив **в IMAPIContainer::GetContentsTable**.
    
3. Создайте ограничение на основе свойств [PidTagConversationKey](https://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) **(PR_CONVERSATION_KEY),** **PidTagSearchKey** **(PR_SEARCH_KEY)** и [Свойств PidTagMessageClass](https://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) **(PR_MESSAGE_CLASS),** чтобы получить таблицу, содержаную все скрытые сообщения в связанном содержимом почтового ящика. Ниже приводится пример ограничения, извлеченного из [Locating the POP3 UIDL History](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx).
    
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

4. Из таблицы найдите скрытое сообщение с помощью **IMAPITable::FindRow**.
    
5. Если на шаге 4 не удается найти скрытое сообщение, измените ограничение на использование **PidTagSearchKey** **(PR_SEARCH_KEY)** вместо **PidTagConversationKey,** как показано ниже:
    
   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. Найдите скрытое сообщение **с помощью IMAPITable::FindRow**. 
    
7. Если шаг 6 не удается, измените ограничение на использование [PidTagSubject](https://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) **(PR_SUBJECT),** равное следующему значению (показано ниже с помощью замены стиля для  `printf` краткости). 
    
   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. Найдите скрытое сообщение с помощью **IMAPITable::FindRow**.
    
9. Если вы работаете Outlook 2010 или более поздней версии, используйте следующие значения **для PidTagProfileName** **(PR_PROFILE_NAME)** и **PidTagSearchKey** **(PR_SEARCH_KEY),** соответственно.
    
   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   Выполнить действия с 3 по 8. Если при этом не удается найти сообщение, возвращайся к исходным шагам 3-8.
    
10. Откройте скрытое сообщение, найденное в шаге 4, 6 или 8.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a>Поиск соответствующего вложения скрытого сообщения

Поскольку скрытое сообщение может иметь несколько вложений, найми соответствующее вложение в следующем порядке.
  
> [!NOTE]
> Эта процедура снова использует  `printf` замену стиля для краткости. 

1. Найди вложение, в котором [PidTagAttachLongFilename](https://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) **(PR_ATTACH_LONG_FILENAME)** соответствует следующей строке, где находится SMTP-адрес пользователя, как указано в профиле  `szEmailAddress` пользователя. . 
    
   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. Найди вложение, у которого [PidTagAttachFilename](https://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) **(PR_ATTACH_FILENAME)** совпадает с "BlobPOP%s",  `szEmailAddress` .
    
3. Найди вложение, имя [которого в PidTagDisplayName](https://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) **(PR_DISPLAY_NAME)** совпадает с "BlobPOP%s",  `szEmailAddress` .
    
4. Иском вложение, в котором **PidTagAttachFilename** **(PR_ATTACH_FILENAME)** совпадает с "Blob%.8x", откуда исходит  `dwAcctUID`  `dwAcctUID` [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md). Вы можете использовать [метод IOlkAccount::GetProp](iolkaccount-getprop.md) для доступа к **свойству PROP_ACCT_MINI_UID.** 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a>Доступ к свойству PidTagAttachDataBinary вложения сообщения

После размещения соответствующего вложения скрытого сообщения используйте **IMAPIProp::GetProps** для чтения свойства **PidTagAttachDataBinary** вложения. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a>

## <a name="next-steps"></a>Дальнейшие действия

В этом разделе вы узнали, как найти историю скачивания сообщений для почтового клиента POP3. Чтобы [](parsing-the-message-download-history-for-a-pop3-account.md) узнать, как размыть эту историю, чтобы определить сообщения, которые были загружены или удалены для почтового ящика, см. в этой записи. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a>

## <a name="see-also"></a>См. также

- [Управление скачиванием сообщений для учетных записей POP3](managing-message-downloads-for-pop3-accounts.md)   
- [Анализ журнала скачивания сообщений для учетной записи POP3](parsing-the-message-download-history-for-a-pop3-account.md)
- [Поиск истории UIDL POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    

