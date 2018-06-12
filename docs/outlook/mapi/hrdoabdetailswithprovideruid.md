---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: fada57c45602f0a0b07276034101fa23a7525f5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808662"
---
# <a name="hrdoabdetailswithprovideruid"></a>HrDoABDetailsWithProviderUID

  
  
**Применимо к**: Outlook 
  
Гарантирует, что метод **OpenEntry** открывается с ожидаемый Exchange доступа к адресной книге. Эта функция работает так же, [IAddrBook::Details](iaddrbook-details.md) , но открывается с помощью адресная книга Exchange, определяемую средством _pEmsabpUID_ **entryID** .
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithProviderUID(
  const MAPIUID   *pEmsabpUID,
  LPADRBOOK        pAddrBook,
  ULONG_PTR FAR *  lpulUIParam,
  LPFNDISMISS      lpfnDismiss,
  LPVOID           lpvDismissContext,
  ULONG            cbEntryID,
  LPENTRYID        lpEntryID,
  LPFNBUTTON       lpfButtonCallback,
  LPVOID           lpvButtonContext,
  LPSTR           lpszButtonText,
  ULONG            ulFlags
);
```

## <a name="parameters"></a>Parameters

 _pEmsabpUID_
  
> [in] Указатель на _emsabpUID_ , который определяет поставщик адресной книги Exchange этой функции следует использовать для отображения сведений на идентификатор записи. Если входящий идентификатор записи не идентификатор записи адресной книги Exchange поставщика, этот параметр игнорируется и действует вызова функции аналогично [IAddrBook::Details](iaddrbook-details.md). Если этот параметр имеет значение NULL или ноль MAPIUID, эта функция также работает так же, как [IAddrBook::Details](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] В адресной книге используется для открытия идентификатор записи. Он не может быть NULL.
    
 _lpulUIParam_
  
> [out] Дескриптор родительского окна для диалогового окна.
    
 _lpfnDismiss_
  
> [in] Указатель на функцию, на основе **DISMISSMODELESS** прототип, или значение NULL. Этот член применим только к безрежимным версии диалоговом окне, указанной флагом DIALOG_SDI задаваемая. MAPI вызывает **DISMISSMODELESS** функцию, если пользователь не закрывает диалоговом окне безрежимным адреса клиента, который вызывает диалоговое окно не является активной подробные сведения о том. 
    
 _lpvDismissContext_
  
> [in] Указатель на сведения о контексте для передачи **DISMISSMODELESS** функции, с помощью параметра _lpfnDismiss_ . Этот параметр применяется только к безрежимным версии диалогового окна, включая флаг **DIALOG_SDI** с помощью параметра _ulFlags_ . 
    
 _cbEntryID_
  
> [in] Количество байтов идентификатор записи, указанные с помощью параметра _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи, который представляет записи адресной книги, чтобы открыть.
    
 _lpfButtonCallback_
  
> [in] Указатель на функцию на основании прототипа функции **LPFNBUTTON** . В функции **LPFNBUTTON** добавляется кнопка в диалоговом окне "Подробности". 
    
 _lpvButtonContext_
  
> [in] Указатель на данные, используемый в качестве параметра для функции, указанного с помощью параметра _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> [in] Указатель на строку, которая содержит текст, который применяется для кнопки добавлены, если эта кнопка является расширяемым. Значение параметра _lpszButtonText_ должно быть значение NULL, когда расширяемая кнопка не требуется. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип текста для параметра _lpszButtonText_ . Можно задать следующие флажки: 
    
AB_TELL_DETAILS_CHANGE
  
> Указывает, что сведения о возвращает TRUE, если фактически изменений на адрес; в противном случае сведения о возвращает значение FALSE.
    
DIALOG_MODAL
  
> Отображает модальное версию стандартным диалоговым окном адрес. Этот флаг является взаимоисключающим с DIALOG_SDI.
    
DIALOG_SDI
  
> Отображает безрежимным версию стандартным диалоговым окном адрес. Этот флаг является взаимоисключающим с DIALOG_MODAL.
    
MAPI_UNICODE
  
> Строки переданное хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    

