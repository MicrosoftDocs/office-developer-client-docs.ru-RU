---
title: Constants (Account management API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2a15e5df-b8e3-9c37-b1ee-2881d010e30b
description: В этом разделе содержит определения констант, класс идентификаторы и идентификаторы интерфейса API для управления учетными записями.
ms.openlocfilehash: b9db04e8847748375f4958855a5813e050b1047b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807710"
---
# <a name="constants-account-management-api"></a>Constants (Account management API)

В этом разделе содержит определения констант, класс идентификаторы и идентификаторы интерфейса API для управления учетными записями.
  
## <a name="constants"></a>Константы

|**Constant**|**Определение**|
|:-----|:-----|
|ACCT_INIT_NOSYNCH_MAPI_ACCTS  <br/> |0x00000001  <br/> |
|ACCT_INIT_NO_STORES_CHECK  <br/> |0x00000002  <br/> |
|ACCTUI_NO_WARNING  <br/> |0x0100  <br/> |
|ACCTUI_SHOW_ACCTWIZARD  <br/> |0x0400  <br/> |
|ACCTUI_SHOW_DATA_TAB  <br/> |0x0200  <br/> |
|E_ACCT_NOT_FOUND  <br/> |0x800C8101  <br/> |
|E_ACCT_UI_BUSY  <br/> |0x800C8102  <br/> |
|E_ACCT_WRONG_SORT_ORDER  <br/> |0x800C8105  <br/> |
|E_INVALIDARG  <br/> | *Определенные в файле winerror.h файл заголовка Windows Software Development Kit (SDK).*  <br/> |
|E_NOTIMPL  <br/> | *Определенные в файле winerror.h файл заголовка пакета SDK Windows.*  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |0x800C8002  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |0x800C8005  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |0x800C8003  <br/> |
|E_OLK_PROP_READ_ONLY  <br/> |0x800C800D  <br/> |
|E_OLK_REGISTRY  <br/> |0x800C8001  <br/> |
|Приступая к работе с ENCRYPT_ следующие константы используются в свойстве [PROP_SMTP_SECURE_CONNECTION](prop_smtp_secure_connection.md) для определения тип шифрованного подключения.  <br/> ||
|ENCRYPT_CONN_AUTO  <br/> |3  <br/> |
|ENCRYPT_CONN_NO_SECURITY  <br/> |0  <br/> |
|ENCRYPT_CONN_SSL  <br/> |1  <br/> |
|ENCRYPT_CONN_TLS  <br/> |2  <br/> |
|MAPIACCT_SEND_ONLY  <br/> |0x00000001  <br/> |
|NOTIFY_ACCT_CHANGED  <br/> |1  <br/> |
|NOTIFY_ACCT_CREATED  <br/> |2  <br/> |
|NOTIFY_ACCT_DELETED  <br/> |3  <br/> |
|NOTIFY_ACCT_ORDER_CHANGED  <br/> |4  <br/> |
|NOTIFY_ACCT_PREDELETED  <br/> |5  <br/> |
|OLK_ACCOUNT_NO_FLAGS  <br/> |0  <br/> |
|ЗНАЧЕНИЕ S_OK  <br/> | *Определенные в файле winerror.h файл заголовка пакета SDK Windows.*  <br/> |
|S_FALSE  <br/> | *Определенные в файле winerror.h файл заголовка пакета SDK Windows.*  <br/> |
|SECURE_FLAG  <br/> |0x8000  <br/> |
|Следующие константы, начиная с SMTP_ используется в свойстве [PROP_SMTP_AUTH_METHOD](prop_smtp_auth_method.md) и укажите метод проверки подлинности.  <br/> ||
|SMTP_AUTH_SAME_AS_POP  <br/> |0  <br/> |
|SMTP_AUTH_RECEIVE_BEFORE_SEND  <br/> |2  <br/> |
|SMTP_AUTH_USER_PASS  <br/> |1  <br/> |
|Следующие константы 5 и макросы используется в свойстве [PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md) и укажите параметры для учетной записи POP Оставлять копии сообщений на сервере.  <br/> ||
|LEAVE_ON_SERVER  <br/> |0x1  <br/> |
|REMOVE_AFTER  <br/> |0x2  <br/> |
|REMOVE_ON_NUKE  <br/> |0x4  <br/> |
|GET_REMOVE_AFTER_DAYS(UL)  <br/> |((ul)\>\>16)  <br/> |
|SET_REMOVE_AFTER_DAYS(days)  <br/> |((дней)\<\<16)  <br/> |
   
## <a name="class-identifiers"></a>Идентификаторы класса

Используйте макрос DEFINE_GUID определенные в guiddef.h файл заголовков Windows SDK для сопоставления символическое имя GUID с его значение.
  
{ed475410-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkAccountManager 0xed475410, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0х2А, 0x66, 0x76); 
  
{ed475411-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkPOP3Account 0xed475411, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0х2А, 0x66, 0x76);
  
{ed475412-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkIMAP4Account 0xed475412, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0х2А, 0x66, 0x76);
  
{ed475414-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkMAPIAccount 0xed475414, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0х2А, 0x66, 0x76);
  
{ed475418-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkMail 0xed475418, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0х2А, 0x66, 0x76);
  
{ed475419-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkAddressBook 0xed475419, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0х2А, 0x66, 0x76);
  
{ed475420-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkStore 0xed475420, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0х2А, 0x66, 0x76);
  
{4db5cbf0-3b77-4852-bc8e-bb81908861f3}
  
DEFINE_GUID (CLSID_OlkHotmailAccount 0x4db5cbf0, 0x3b77, 0x4852, 0xbc, 0x8e, 0xbb, 0x81, 0x90, 0x88, 0x61, 0xf3);
  
{4db5cbf2-3b77-4852-bc8e-bb81908861f3}
  
DEFINE_GUID (CLSID_OlkLDAPAccount 0x4db5cbf2, 0x3b77, 0x4852, 0xbc, 0x8e, 0xbb, 0x81, 0x90, 0x88, 0x61, 0xf3);
  
## <a name="interface-identifiers"></a>Идентификаторы интерфейса

Используйте макрос DEFINE_GUID определенные в guiddef.h файл заголовков Windows SDK для сопоставления символическое имя GUID с его значение.
  
{9240A6C0-AF41-11d2-8C3B-00104B2A6676}
  
DEFINE_GUID (IID_IOlkErrorUnknown 0x9240a6c0, 0xaf41, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0х2А, 0x66, 0x76);
  
{9240A6C1-AF41-11d2-8C3B-00104B2A6676}
  
DEFINE_GUID (IID_IOlkEnum 0x9240a6c1, 0xaf41, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0х2А, 0x66, 0x76);
  
{9240a6c3-af41-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccountNotify 0x9240a6c3, 0xaf41, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0х2А, 0x66, 0x76);
  
{9240a6cb-af41-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccountHelper 0x9240a6cb, 0xaf41, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0х2А, 0x66, 0x76); 
  
{9240a6cd-af41-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccountManager 0x9240a6cd, 0xaf41, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0х2А, 0x66, 0x76); 
  
{9240a6d2-af41-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccount 0x9240a6d2, 0xaf41, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0х2А, 0x66, 0x76);
  

