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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270100"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает интерфейс [имапиформмгр](imapiformmgriunknown.md) для объекта поставщика библиотеки форм в контексте существующего сеанса. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиформ. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a>Параметры

 _Псессион_
  
> возврата Указатель на сеанс, используемый клиентским приложением.
    
 _ппмгр_
  
> вышли Указатель на возвращенный интерфейс **имапиформмгр** . 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

После того как клиентское приложение вызовет функцию **мапиопенформмгр** , большинство последующих взаимодействий, связанных с формами, выполняются через поставщика библиотеки форм или через интерфейс, возвращенный поставщиком библиотеки форм. Интерфейс **имапиформмгр** позволяет клиенту работать с обработчиками сообщений и выполнять разрешения между классами сообщений и библиотеками форм. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Маиндлг. cpp открывает Диспетчер форм, чтобы можно было выбрать форму.  <br/> |Кмаиндлг:: Онселектформ  <br/> |MFCMAPI использует метод **мапиопенформмгр** , чтобы открыть Диспетчер форм, чтобы можно было выбрать форму.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

