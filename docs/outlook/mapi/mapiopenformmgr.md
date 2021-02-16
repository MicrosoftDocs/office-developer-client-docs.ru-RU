---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: de0c1181450c536dffd5a84242c17bd1dd612566
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418052"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает интерфейс [IMAPIFormMgr](imapiformmgriunknown.md) для объекта поставщика библиотеки форм в контексте существующего сеанса. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a>Параметры

 _pSession_
  
> [in] Указатель на сеанс, который использует клиентский приложение.
    
 _ppmgr_
  
> [out] Указатель на возвращенный **интерфейс IMAPIFormMgr.** 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

После вызова функции **MAPIOpenFormMgr** клиентского приложения большинство последующих взаимодействий, связанных с формами, происходит через поставщика библиотеки форм или интерфейс, возвращенный поставщиком библиотеки форм. Интерфейс **IMAPIFormMgr** позволяет клиенту работать с обработчиками сообщений и выполнять разрешения между классами сообщений и библиотеками форм. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MainDlg.cpp открывает диспетчер форм, чтобы можно было выбрать форму.  <br/> |CMainDlg::OnSelectForm  <br/> |MFCMAPI использует метод **MAPIOpenFormMgr** для открытия диспетчера форм, чтобы можно было выбрать форму.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

