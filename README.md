    @Override
    public boolean getFollowup(CardHand cards) {
        int poker3 = Poker.POINTS_VALUES.get(cards.getPoker3().getPoint());
        int poker2 = Poker.POINTS_VALUES.get(cards.getPoker2().getPoint());

        if(cards.getCardsType()==CardHand.HAND_TYPE_VALUE_HIC
                && Poker.POINTS_VALUES.get(cards.getPoker3().getPoint())<=12){
                && (poker3<12 || (poker3==12 && poker2<6))){
            return false;
        }
