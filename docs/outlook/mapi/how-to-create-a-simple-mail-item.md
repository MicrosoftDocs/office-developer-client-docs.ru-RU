---
title: Создание простого почтового элемента
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bbf99c4b-3008-4475-a60a-648eaed59d01
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8b7afa8f3c04cb479906f721db8de90e8cf66f11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345195"
---
# <a name="create-a-simple-mail-item"></a>Создание простого почтового элемента
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
С помощью MAPI можно создавать и отправлять сообщения, запрашивающие уведомление о прочтении. Когда запрашивается уведомление о прочтении, система обмена сообщениями создает и возвращает отчет о прочтении отправителю при открытии сообщения получателем.
  
Сведения о том, как скачать, просмотреть и запустить код из приложения MFCMAPI и проекта Креатеаутлукитемсаддин, указанного в этом разделе, приведены в статье [Установка примеров, используемых в этом разделе](how-to-install-the-samples-used-in-this-section.md).


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a>Создание и отправка сообщения с запросом уведомления о прочтении

1. Создайте исходящее сообщение. Сведения о создании исходящих сообщений содержатся в разделе [Обработка исходящих сообщений](handling-an-outgoing-message.md).
    
2. Добавьте свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) и задайте для него значение **true**.
    
3. Добавьте свойство **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)).
    
4. Добавьте свойство **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)).
    
5. Отправьте сообщение, вызвав метод [iMessage:: субмитмессаже](imessage-submitmessage.md) . 
    
Эти `AddMail` шаги демонстрируются в функциях исходного файла mails. cpp в проекте креатеаутлукитемсаддин. `AddMail` Функция принимает параметры из диалогового окна **Добавление почты** , которое отображается при выборе команды **Добавить почту** в меню **надстройки** примера приложения MFCMAPI. `DisplayAddMailDialog` Функция в разделе mails. cpp отображает диалоговое окно и передает значения из диалогового окна `AddMail` функции. `DisplayAddMailDialog` Функция не связана напрямую с созданием почтового элемента с помощью MAPI, поэтому она не указана здесь. `AddMail` Функция указана ниже. 
  
Обратите внимание, что параметр _лпфолдер_ , `AddMail` передаваемый в метод, является указателем на интерфейс [IMAPIFolder](imapifolderimapicontainer.md) , представляющий папку, в которой будет создано новое сообщение. При наличии параметра _лпфолдер_ , представляющего интерфейс **IMAPIFolder** , код вызывает метод [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) . Метод **CreateMessage** возвращает код успешного выполнения и указатель на указатель на интерфейс [iMessage: IMAPIProp](imessageimapiprop.md) . 

Большая часть кода `AddMail` функции обрабатывает работу по настройке свойств при подготовке к вызову метода [IMAPIProp:: SetProps](imapiprop-setprops.md) . При успешном вызове метода **SetProps** вызов метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) фиксирует изменения в хранилище и создает новый элемент почты. Затем, при запросе, вызывается метод [iMessage:: субмитмессаже](imessage-submitmessage.md) для отправки сообщения. 
  
`AddMail` Функция использует две вспомогательные функции для создания значений свойств **PR_CONVERSATION_INDEX** и **PR_REPORT_TAG** : функции `BuildConversationIndex` и. `AddReportTag` Функция, расположенная в Креатеаутлукитемсаддин. cpp, выполняет те же действия, что и встроенная функция MAPI Сккреатеконверсатиониндекс, когда родительский индекс беседы не передается. [ScCreateConversationIndex](sccreateconversationindex.md) `BuildConversationIndex` Формат буфера индекса беседы, который создает эти функции, описан в [каноническое свойство PidTagConversationIndex](pidtagconversationindex-canonical-property.md). 

`AddReportTag` Функция, расположенная в разделе mails. cpp, в свою очередь `BuildReportTag` вызывает функцию для создания структуры для свойства **PR_REPORT_TAG** . Сведения о структуре, которая создает `BuildReportTag` функция, можно найти в статье [PidTagReportTag каноническое свойство](pidtagreporttag-canonical-property.md).
  
Ниже приведен полный список `AddMail` функции. 
  
```cpp
HRESULT AddMail(LPMAPISESSION lpMAPISession,
            LPMAPIFOLDER lpFolder,
            LPWSTR szSubject, // PR_SUBJECT_W, PR_CONVERSATION_TOPIC
            LPWSTR szBody, // PR_BODY_W
            LPWSTR szRecipientName, // Recipient table
            BOOL bHighImportance, // PR_IMPORTANCE
            BOOL bReadReceipt, // PR_READ_RECEIPT_REQUESTED
            BOOL bSubmit,
            BOOL bDeleteAfterSubmit)
{
   if (!lpFolder) return MAPI_E_INVALID_PARAMETER;
   HRESULT hRes = S_OK;
   LPMESSAGE lpMessage = 0;
   // Create a message and set its properties
   hRes = lpFolder->CreateMessage(0,
      0,
      &lpMessage);
   if (SUCCEEDED(hRes))
   {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
      SPropValue spvProps[NUM_PROPS] = {0};
      spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag          = PR_MESSAGE_CLASS_W;
      spvProps[p_PR_ICON_INDEX].ulPropTag                 = PR_ICON_INDEX;
      spvProps[p_PR_SUBJECT_W].ulPropTag                = PR_SUBJECT_W;
      spvProps[p_PR_CONVERSATION_TOPIC_W].ulPropTag     = PR_CONVERSATION_TOPIC_W;
      spvProps[p_PR_BODY_W].ulPropTag                   = PR_BODY_W;
      spvProps[p_PR_IMPORTANCE].ulPropTag               = PR_IMPORTANCE;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].ulPropTag   = PR_READ_RECEIPT_REQUESTED;
      spvProps[p_PR_MESSAGE_FLAGS].ulPropTag             = PR_MESSAGE_FLAGS;
      spvProps[p_PR_MSG_EDITOR_FORMAT].ulPropTag         = PR_MSG_EDITOR_FORMAT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].ulPropTag         = PR_MESSAGE_LOCALE_ID;
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].ulPropTag = PR_INETMAIL_OVERRIDE_FORMAT;
      spvProps[p_PR_DELETE_AFTER_SUBMIT].ulPropTag      = PR_DELETE_AFTER_SUBMIT;
      spvProps[p_PR_INTERNET_CPID].ulPropTag            = PR_INTERNET_CPID;
      spvProps[p_PR_CONVERSATION_INDEX].ulPropTag         = PR_CONVERSATION_INDEX;
      spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Note";
      spvProps[p_PR_ICON_INDEX].Value.l = 0x103; // Unsent Mail
      spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
      spvProps[p_PR_CONVERSATION_TOPIC_W].Value.lpszW = szSubject;
      spvProps[p_PR_BODY_W].Value.lpszW = szBody;
      spvProps[p_PR_IMPORTANCE].Value.l = bHighImportance?IMPORTANCE_HIGH:IMPORTANCE_NORMAL;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].Value.b = bReadReceipt?true:false;
      spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_UNSENT;
      spvProps[p_PR_MSG_EDITOR_FORMAT].Value.l = EDITOR_FORMAT_PLAINTEXT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].Value.l = 1033; // (en-us)
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].Value.l = NULL; // Mail system chooses default encoding scheme
      spvProps[p_PR_DELETE_AFTER_SUBMIT].Value.b = bDeleteAfterSubmit?true:false;
      spvProps[p_PR_INTERNET_CPID].Value.l = cpidASCII;
      hRes = BuildConversationIndex(
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.cb,
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb);
      if (SUCCEEDED(hRes))
      {
         hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
         if (SUCCEEDED(hRes))
         {
            hRes = AddRecipient(lpMAPISession,
               lpMessage,
               MAPI_TO,
               szRecipientName);
            AddInLog(true,L"CallMenu: AddRecipient - returned hRes = 0x%08X\n",hRes);
            if (SUCCEEDED(hRes))
            {
               if (bReadReceipt)
               {
                  hRes = AddReportTag(lpMessage);
               }
               if (SUCCEEDED(hRes))
               {
                  hRes = lpMessage->SaveChanges(KEEP_OPEN_READWRITE);
                  if (SUCCEEDED(hRes) && bSubmit)
                  {
                     hRes = lpMessage->SubmitMessage(NULL);
                  }
               }
            }
         }
      }
      if (spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb)
         delete[] spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb;
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}
```

## <a name="see-also"></a>См. также

- [Использование MAPI для создания элементов Outlook 2007](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

