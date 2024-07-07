# Assignment-1
Trigger 1---
DELIMITER 1/
CREATE TRIGGER update wallet AFTER INSERT ON payment details
FOR EACH ROW
BEGIN
IF NEW.payment type wallet* THEN
UPDATE customer details
SET wallet-wallet-NEW.fare WHERE customer_id-(SELECT customer_id FROM booking details WHERE booking_ id-NEW.booking_id);
END IF:
END;
INSERT INTO payment_details VALUES(*PK200", 'BK222', 45,5, NULL, 5, wallet*,4.2, 'OKAY") -> can't insert due to foreign key constraint as child referring to booking details
Trigger 2---
DELIMITER/I
CREATE TRIGGER update rating AFTER UPDATE ON payment_details
FOR EACH ROW
BEGIN
DECLARE tot_rating INT;
DECLARE tot_rating sum FLOAT;
DECLARE new avg rating FLOAT;
BE NEW.driver_rating IS NOT NULL AND NEW.driver_rating OLD.driver_rating THEN
SELECT COUNT (*), SUM(driver_rating) INTO tot_rating, tot_rating_sum FROM payment_details WHERE payment_id=NEW.payment_id AND driver_rating IS NOT HULL;
SET new averating tot_rating_sum/tot_rating;
UPDATE driver details
SET average_rating-new_aygrating WHERE driver_id=(SELECT driver_id FROM booking_details WHERE booking_id - (SELECT booking_id FROM payment details WHERE
Trigger 3---
DELIMITER 1/
CREATE TRIGGER upgrade coupon details AFTER DELETE ON booking details
FOR EACH ROW
BEGIN
DECLARE can_count INT;
DECLARE new coupon VARCHAR(50);
DECLARE sEC VARCHAR(50);
DECLARE des VARCHAR (50);
DECLARE exist INT DEFAULT 0;
SELECT COUNT (booking_id) INTO can_count FROM booking details WHERE source-OLD.source AND destination-OLD.destination AND booking status-'cancelled*;
IF can count>3 THEN
SET soc-SUBSTRING(OLD. source, 1,2);
SET des=SUBSTRING(OLD destination, 1,2);
SET new _coupon=CONCAT(*OFFER', sec, des);
SELECT COUNT*) INTO exist FROM coupon _details WHERE coupon_code=new_coupon;
IF exist› THEN
CALL update_ coupons)
ELSE
INSERT INTO coupon details VALUES(new_coupon, (SELECT current_date + INTERVAL 5 day), 'Claim maximum offers using this coupon*, (3*can _count));
END IF;
END IF;
END;
