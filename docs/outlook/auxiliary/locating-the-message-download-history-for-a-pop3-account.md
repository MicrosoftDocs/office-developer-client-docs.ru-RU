---
title: Поиск журнала скачивания сообщений для учетной записи POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: В этом разделе описывается, как почтовый клиент может получить доступ к свойству PidTagAttachDataBinary, чтобы получить журнал загрузки сообщений для учетной записи POP3.
ms.openlocfilehash: ae12a044098aa4f42e1c2e5936e82da3d7a128dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321877"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a>Поиск журнала скачивания сообщений для учетной записи POP3

В этом разделе описывается, как почтовый клиент может получить доступ к свойству [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) , чтобы получить журнал загрузки сообщений для учетной записи POP3. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a>

## <a name="why-get-the-message-download-history"></a>Зачем получать историю загрузки сообщений?

Поставщик услуг POP (Post Office Protocol) для Outlook позволяет пользователям получать и загружать новые сообщения электронной почты на их локальных устройствах, а затем оставлять и удалять эти сообщения на почтовом сервере. Когда почтовый клиент проверяет, нужно ли загружать новые сообщения, он должен иметь возможность определять и загружать только новые сообщения для папки "Входящие". Почтовый клиент выполняет это сначала с помощью команды UIDL (уникальный идентификатор), которая получает карту каждого сообщения, которое когда-либо было доставлено в папку "Входящие", по уникальному идентификатору (UID). Кроме того, клиент получает журнал загрузки сообщений для сообщений, которые были скачаны или удалены из папки "Входящие" этого клиента. После этого клиент может определить, что сообщения отсутствуют в журнале как новые и, следовательно, будут загружаться с помощью записи UID и журнала.
  
Чтобы получить журнал загрузки сообщений для папки "Входящие", выполните следующие действия.
  
- Выполните действия, описанные в этом разделе, чтобы найти свойство **PidTagAttachDataBinary** , которое содержит историю в большом двоичном ОБЪЕКТЕ (BLOB), которая соответствует определенному формату. 
    
- Продолжите [Анализ журнала загрузки сообщений для учетной записи POP3](parsing-the-message-download-history-for-a-pop3-account.md), в которой описано, как проанализировать этот большой двоичный объект, чтобы определить сообщения, которые были скачаны или удалены для этой папки.
    
## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a>Основные понятия, которые необходимо знать при поиске истории загрузки сообщений

Журнал загрузки сообщений для папки "Входящие" хранится в двоичном свойстве MAPI **PidTagAttachDataBinary**для вложения скрытого сообщения в папку "Входящие". В таблице 1 показаны ресурсы для концепций, которые помогут вам узнать, как определить расположение журнала загрузки сообщений.
  
**Таблица 1. Основные понятия**

|**Название статьи**|**Описание**|
|:-----|:-----|
|[Скрытые папки MAPI](https://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |MAPI позволяет почтовым клиентам хранить информацию в скрытых папках и скрытых сообщениях. Скрытые папки находятся в связанной части папок MAPI и обычно содержат сведения, которые не являются видимыми для пользователей и не могут управлять ими. Клиенты выбирают формат и содержимое, которые должны храниться в скрытых папках в скрытых папках.  <br/> |
|[Сообщения MAPI](https://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |MAPI хранит сообщения в папках либо в стандартном поддереве IPM, которое видимо пользователям клиента, либо вне поддерева и невидимо для пользователей. Сообщения могут содержать дополнительные данные, хранящиеся в вложении, которое может быть представлено в виде файла, другого сообщения или объекта OLE. В случае истории загрузки сообщений Журнал хранится в свойстве сообщения, которое присоединено к другому скрытому сообщению.  <br/> |
|[Общие сведения о свойствах сообщений](https://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |Когда клиент сохраняет информацию в сообщении, он фактически сохраняет их в свойстве сообщения. MAPI поддерживает много свойств — некоторые из них всегда существуют и могут устанавливаться клиентами, другие являются необязательными, а клиенты не могут ожидать, что они доступны или установлены в допустимые значения. Журнал загрузки сообщения хранится в свойстве **PidTagAttachDataBinary** вложения в скрытом сообщении.  <br/> |
|[Профили MAPI](https://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |Во время входа в сеансе почтовый клиент выбирает профиль, описывающий поставщиков и службы, которые необходимо использовать. Профиль разбивается на разделы, содержащие свойства. В частности, свойства [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) и [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) (**PR_PROFILE_NAME**) всегда существуют. Ключ поиска профиля уникален для всех профилей и хранится в разделе профиля, который определяется **MUID_PROFILE_INSTANCE** (который ОПРЕДЕЛЕН в мапигуид. H). Используйте [IMAPISession:: опенпрофилесектион](https://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx) , чтобы открыть раздел, и используйте [IMAPIProp:: Prop](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) для получения значений свойств.  <br/> |
|[Таблицы содержимого](https://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |Поставщики хранилищ сообщений реализуют таблицы содержимого для их папок. Для скрытых сообщений в связанной части папки поставщики хранилищ сообщений поддерживают связанные таблицы содержимого, а клиенты могут использовать метод [IMAPIContainer:: жетконтентстабле](https://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx) , чтобы вернуть указатель на связанную таблицу содержимого.  <br/> |
|[Сведения об ограничениях](https://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [Типы ограничений](https://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [Создание ограничения](https://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [Пример кода ограничения](https://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |В MAPI клиенты могут использовать ограничения для фильтрации таблиц содержимого, чтобы выполнять поиск по строкам, представляющим сообщения, для которых задано определенное свойство с определенным значением. Ограничения определяются с помощью структуры данных [срестриктион](https://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx) , которая может содержать объединение более специализированных структур ограничений. Метод [IMAPITable:: FindRow](https://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx) применяет ограничение и извлекает из таблицы первую строку, которая соответствует условиям ограничения.  <br/> |
|[Сведения о регистрации хранилищ для индексирования](https://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |С помощью свойства [PidTagStoreProvider](https://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) (**PR_MDB_PROVIDER**) Проверьте тип поставщика хранилища. Например, чтобы проверить, является ли хранилище хранилищем Exchange, свойство **PidTagStoreProvider** должно возвращать значение, представленное константным **пбексчанжепровидерпримарюсергуид**, которое определено в файле общедоступного заголовка едкмдб. h.  <br/> |
   
## <a name="locating-the-appropriate-hidden-message-and-attachment"></a>Поиск соответствующего скрытого сообщения и вложения

Теперь, когда мы знаем, что журнал загрузки сообщений для папки "Входящие" находится в свойстве **PidTagAttachDataBinary** вложения в скрытое сообщение, процедура обнаружения соответствующего вложения в соответствующем скрытом сообщении состоит из следующих процедур: 
  
1. [Поиск соответствующего скрытого сообщения](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)
    
2. [Поиск подходящего вложения в скрытом сообщении](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)
    
3. [Доступ к свойству PidTagAttachDataBinary вложения сообщения](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a>

### <a name="find-the-appropriate-hidden-message"></a>Поиск соответствующего скрытого сообщения

1. Получите свойство [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) из профиля в разделе profile, заданном **MUID_PROFILE_INSTANCE**.
    
2. Откройте связанное содержимое папки "Входящие", вызвав **IMAPIContainer:: жетконтентстабле**.
    
3. Создайте ограничение на основе свойств [PidTagConversationKey](https://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (**PR_CONVERSATION_KEY**), **PidTagSearchKey** (**PR_SEARCH_KEY**) и [PidTagMessageClass](https://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) (**PR_MESSAGE_CLASS**), чтобы получить таблицу, содержащую все скрытые сообщения в связанном содержимом папки "Входящие". Ниже приведен пример ограничения, извлеченного из [поиска журнала протокола POP3 UIDL](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx).
    
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

4. В таблице найдите скрытое сообщение с помощью **IMAPITable:: FindRow**.
    
5. Если на шаге 4 не удается найти скрытое сообщение, измените ограничение на использование **PidTagSearchKey** (**PR_SEARCH_KEY**) вместо **PidTagConversationKey**, как показано ниже:
    
   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. Найдите скрытое сообщение, используя **IMAPITable:: FindRow**. 
    
7. Если не удается выполнить шаг 6, измените ограничение на использование [PidTagSubject](https://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**PR_SUBJECT**) равным приведенному ниже значению (показано `printf` ниже, в котором для краткости используется подстановочный стиль). 
    
   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. Найдите скрытое сообщение с помощью **IMAPITable:: FindRow**.
    
9. Если вы используете Outlook 2010 или более поздней версии, используйте следующие значения для **PidTagProfileName** (**PR_PROFILE_NAME**) и **PidTagSearchKey** (**PR_SEARCH_KEY**) соответственно.
    
   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   Выполните шаги 3 – 8. Если не удается найти сообщение, вернитесь к исходным шагам 3 – 8.
    
10. Откройте скрытое сообщение, найденное на шаге 4, 6 или 8.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a>Поиск подходящего вложения в скрытом сообщении

Так как скрытое сообщение может иметь несколько вложений, найдите соответствующее вложение в следующем порядке.
  
> [!NOTE]
> Эта процедура снова использует подстановку `printf` стиля для краткости. 

1. Найдите вложение, [PidTagAttachLongFilename](https://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) которого соответствует следующей строке, где `szEmailAddress` — это SMTP-адрес пользователя, как указано в профиле пользователя. . 
    
   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. Найдите вложение, `szEmailAddress` [PidTagAttachFilename](https://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) (**PR_ATTACH_FILENAME**) которого совпадает со строкой "блобпоп% s".
    
3. Найдите вложение, `szEmailAddress` [PidTagDisplayName](https://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) (**PR_DISPLAY_NAME**) которого совпадает со строкой "блобпоп% s".
    
4. Найдите вложение, **PidTagAttachFilename** (**PR_ATTACH_FILENAME**) которого соответствует "BLOB-объект%. 8X" `dwAcctUID`, где `dwAcctUID` поступает из [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md). Для доступа к свойству **PROP_ACCT_MINI_UID** можно использовать метод [иолкаккаунт::.](iolkaccount-getprop.md) 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a>Доступ к свойству PidTagAttachDataBinary вложения сообщения

После того как вы назначите вложение с сообщением в скрытом сообщении, используйте **IMAPIProp::-PROPS** , чтобы прочитать свойство **PidTagAttachDataBinary** вложения. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a>

## <a name="next-steps"></a>Дальнейшие действия

Из этого раздела вы узнали, как определить расположение журнала загрузки сообщений для почтового ящика POP3 почтового клиента. Сведения о том, как проанализировать сообщения, скачанные или удаленные для папки "Входящие", можно найти в разделе [Анализ журнала загрузки сообщений для учетной записи POP3](parsing-the-message-download-history-for-a-pop3-account.md) . 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a>

## <a name="see-also"></a>См. также

- [Управление скачиванием сообщений для учетных записей POP3](managing-message-downloads-for-pop3-accounts.md)   
- [Анализ журнала скачивания сообщений для учетной записи POP3](parsing-the-message-download-history-for-a-pop3-account.md)
- [Поиск журнала протокола POP3 UIDL](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    

